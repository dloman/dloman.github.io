---
layout: post
title: "New Mail Script"
date: 2013-10-15 22:28
comments: true
categories: [python, scripts, future hardware projects]
---
Wrote a quick little script today to check and see if I have new email.
I am using the standard imaplib library along with python-ntlm with a imap patch found on https://github.com/xulz/python-ntlm
I didn't really want to save my cleartext password in the script so pickled the ```ImapNtlmAuthHandler```

```
AuthFile = open(SuperCoolFileLocation,'wb')
AuthHandler = IMAPNtlmAuthHandler(r"domain\username", "password")
pickle.dump(AuthHandler, AuthFile)
AuthFile.close()
```

It's probably not much more secure, but it's more secure then saving in plaintext. If I am wrong and there is a better safer way to do it let me know.
<!-- more -->
Here is the the script I use to get the total number of messages.

```
import getpass, imaplib, pickle

def GetNumberOfMessages():
    Mailbox = imaplib.IMAP4("server.address")
      AuthenticationToken = pickle.load(open('/home/dloman/dloman/imap.auth','rb'))
      Mailbox.authenticate("NTLM", AuthenticationToken)
      Mailbox.select(readonly=True)
      Typ, MessageNums = Mailbox.search(None,'UNSEEN')
      if '' in MessageNums:
        return 0
      return len(MessageNums[0].split(' '))


if __name__ == '__main__':
  print print 'Number Of New Messages =',GetNumberOfMessages()
```
