---
title: Removing PPA and GPG key in Ubuntu.
date: "2019-11-05T08:33:06"
author: "Borys"
---

### Remove PPA manually

Find one to be removed by entering:
`ls /etc/apt/sources.list.d/`
When you have the name of the ppa to be removed (e.g. ~fooppa.list~), you can enter:
`sudo rm /etc/apt/sources.list.d/fooppa.list`

Also taka care of removing of the key the repo

```
# list the trusted keys
sudo apt-key list
# remove the key
sudo apt-key del KEY_ID
```

Note: the KEY_ID is the last 8 digits in the pub section, `4C9D 234C` without space

```
/etc/apt/trusted.gpg.d/nilarimogard_ubuntu_webupd8.gpg
------------------------------------------------------
pub   rsa1024 2010-01-20 [SC]
      1DB2 9AFF F6C7 0907 B57A  A31F 531E E72F 4C9D 234C
uid           [ unknown] Launchpad webupd8

```
