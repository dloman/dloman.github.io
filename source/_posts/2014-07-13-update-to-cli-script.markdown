---
layout: post
title: "update to cli script"
date: 2014-07-13 04:45
comments: true
publish: false
categories: [bash, aliases, cli, sed]
---

A while back I wrote a <a href=http://danloman.org/blog/2013/12/19/alternative-for-quick-cli-filesystem-navagation-shortcutting/> little bash function</a>
which automatically create bash aliases for moving around commonly used areas in my file system.
This worked awesomely until one day I was working on a machine where I was not my normal username.
I use a synced bash_alias file, so when I used the alias and moved to edit files in /home/dloman/Source/ and was not the dloman user things got very confusing when I tried to save my edits.
Needless to say it took me awhile of flailing thinking I was completly insane until I figured out what was happening.
I edited the file with the sed command to replace the expanded `$HOME` path with the actual string `$HOME`. The updated command is as follows:

```
function mark
{
  echo "alias $1='cd $(pwd)'" | sed -e "s:$HOME:\$HOME:g" >> ~/Dropbox/Config/bash_aliases ;
  source ~/Dropbox/Config/bash_aliases
}
```
Now my bash_aliases file is sharable regardless of which user I am logged in as.
