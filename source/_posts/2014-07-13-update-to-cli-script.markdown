---
layout: post
title: "update to cli script"
date: 2014-07-13 04:45
comments: true
publish: false
categories: [bash, aliases, cli, sed]
---
A while back I wrote a <a href=http://danloman.org/blog/2013/12/19/alternative-for-quick-cli-filesystem-navagation-shortcutting/> little bash function</a>
which automatically creates bash aliases for moving around in commonly used directories in my file system.
This worked awesomely until one day I was working on a machine where I was not my normal username.
The root of my problem was that I use a synced bash_alias file, so  all of my bash_alias files are identical across multiple machines and users.
normal this works great, but when I used the alias and moved to edit files in what i thought was /home/differentuser/Source/ I was acutally editing /home/dloman/Source/.
I didnt realize this mistake and got very confused when I tried to save my edits and was unable to.
Needless to say it took me awhile of flailing about, thinking I was completly insane until I figured out what was happening.
I edited the my mark function with this sed command to replace the expanded `$HOME` path with the actual string `$HOME`. The updated command is as follows:

```
function mark
{
  echo "alias $1='cd $(pwd)'" | sed -e "s:$HOME:\$HOME:g" >> ~/Dropbox/Config/bash_aliases ;
  source ~/Dropbox/Config/bash_aliases
}
```
Now my bash_aliases file is sharable regardless of which user I am logged in as.
