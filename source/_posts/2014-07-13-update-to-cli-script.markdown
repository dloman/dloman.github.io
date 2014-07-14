---
layout: post
title: "update to cli script"
date: 2014-07-13 04:45
comments: true
publish: false
categories: [bash, aliases, cli, sed]
---
a long while back I wrote some little bash function which automatically create bash aliases for moving around commonly used areas in my file system. This worked awesome until one day I was working on a machine where i was not my normal username. I use a synced bash_alias file when I used the alias and moved to edit files in /home/dloman/Source/ and was not the dloman user things got very confusing when I tried to save my edits. Needless to say it took me awhile of thinking I was completly insane until I figured out what was happening. I edited the file with the sed command to replace the expanded `$HOME` path with the actual string `$HOME`. the command is as follows:

```
function mark
{
  echo "alias $1='cd $(pwd)'" >> ~/Dropbox/Config/bash_aliases ;
  source ~/Dropbox/Config/bash_aliases
}
```
