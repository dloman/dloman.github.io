---
layout: post
title: "Alternative for quick cli filesystem navagation shortcutting"
date: 2013-12-19 22:00
sharing: true
comments: true
categories: [bash, aliases, cli]
---
I saw this great <a href="http://jeroenjanssens.com/2013/08/16/quickly-navigate-your-filesystem-from-the-command-line.html"> blog post</a> about an easy way to create and remove shortcuts for commandline navagation to often used directories.
In the past I would often manually make bash aliases for commonly used directories, so I was psyched to automate this. I much prefer just typing the ```DirName``` instead of the ```jump DirName``` used in Jeroen's version, so I modified his commands with my own.
Here are the commands I came up with.

```
function mark {
  echo "alias $1='cd $(pwd)'" >> ~/Dropbox/Config/bash_aliases ; source ~/Dropbox/Config/bash_aliases
}
function unmark {
  sed -e "/^alias $1='cd/d" -i ~/Dropbox/Config/bash_aliases ; source ~/Dropbox/Config/bash_aliases
}
function marks {
  cat ~/Dropbox/Config/bash_aliases | grep "='cd" | sed -e 's/alias //' -e "s/='cd / \=\> /" -e "s/'$//" -e "/^  echo /d" -e "/&&/d" -e "/^  sed/d"
}
```
<!-- more -->
This may not be the most elegant way of doing things (that sed command is fairly heinous) but it works great.

BTW keeping my bash_aliases file inside of dropbox is amazing...aliases and functions instantly appear on all my machines. It's rad.

P.S. originally I had the ```unmark``` command looking like this

```
}
function unmark {
  sed -e "/^alias $1/d" -i ~/.bash_aliases ; source ~/.bash_aliases
}
```

which seems like a only minor modification from the current version. This seemingly minor change of ```alias $1``` -> ```alias $1='cd``` looks like nothing, but one time I accidentally typed
```
$mark
```
which created the line ```alias ='cd ~/WhereverIWasWhenIDidThis'``` in my ```~/Dropbox/Config/bash_aliases```
realising I just made a empty alias I immediatly tried removing the alias with
```
$unmark
```
which proceded to delete all aliases in my ```~/Dropbox/Config/bash_aliases```!!!
That was interesting, thank goodness for dropbox backing things up (another reason to keep config files in dropbox).
Let me know what you think in the comments or hit me up on twitter.

