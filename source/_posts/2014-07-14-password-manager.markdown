---
layout: post
title: "Password Manager"
date: 2014-07-14 22:22
comments: true
categories: [Android, bash, password management, SHA1, security]
---
Passwords are annoying.
I am not very good at remembering passwords and am even worse at remembering strong passwords.
Even though I am fully aware of how terrible it is to reuse passwords it is just so much easier
and I never forget my 1 password that I pretty much use for everything.
Knowing that this is a terrible way to do handle my passwords and
not really liking storing passwords in an encrypted volume or online password manager I decided to use
hash functions.

<!-- more -->

##Hash Function
according to wikipedia
"a <a href=http://en.wikipedia.org/wiki/Cryptographic_hash_function> cryptographic hash function </a>
is a function which generates fixed-length output data that acts as a shortened reference to the original
data which is considered practically impossible to invert, that is, to recreate the input data from its hash value alone."

This impossibility to invert means that even if my password gets leaked it is impossible to get the string from which my password was generated.
And as long as there are no collisions in the hash function it is guaranteed that all password + website combinations will generate a unique alpha numeric string.

##What my app does
The applications are quite simple.
They take input from the user for a password and website.
They then concatenate those strings together and use that string as an input to SHA1 hash function.
The first 10 digits of the output of the SHA1 function are then copied into the copy/paste buffer
of the system to be pasted into the password field for the site.

##The Code
```
#!/bin/bash
printf "Enter Password Please: "
stty -echo
read pass
printf "\nEnter Website Please: "
stty echo
read site
printf '\n'
echo ${pass/ /}${site/ /} |openssl sha1 |cut -c 10-19|xclip -selection c
history -d $((HISTCMD-0))
exit
```


##Cross Platform
I originally wrote this app as a bash script and used it for almost a year that way.
The issue with this was when i was on my phone I had to log in via ssh run the command
and then copy from the terminal app.
This was a pain, and since this was a very simple application I figured it would be a
good project to learn android development with.
So I wrote an android application which does the exact same thing as the bash script.
Its not the prettiest app in the world but it works great.
you can check out the android app on my
<a href=http://github.com/dloman/PasswordManager.git> Github Page </a>

Let me know if you have any improvements, questions or comments!

