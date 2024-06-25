---
layout: single
title: FTP port enumeration
excerpt: "FTP (File Transfer Protocol) is a communication between the server and the client for transfer files, either for download or upload files."
date: 2024-06-24
classes: wide
header:
  teaser: /assets/images/ftp.jpg
  teaser_home_page: true
  icon: #/assets/images/hackthebox.webp
categories:
  - FTP
  - Protocol
#tags:  
#  - osticket
#  - mysql
#  - mattermost
#  - hashcat
#  - rules
---

The port 21 it's basically the protocol TCP and it's impotant know how to enumerate this port because if you can go into any user, this could be dangerous because you will be able to download and upload files.

For this post we will do a container in docker making a user with a password:

![](/assets/images/picture1.png)

After doing the container, as you can see, if you do a "docker ps" you can see that the port open for this is the port 21 in your localhost.

![](/assets/images/picture2.png)

In this case we're gonna assume that we know already the username but not the password. So what we gonna try to do is, whit burtal force, find the password with "hydra", and for this we're gonna need a dictionary with passwords.
After you got a dictionary you will use hydra.

![](/assets/images/passwordfind.png)

The -l is for put in what user you want to log in, the -P is for the dictionary that you want to use.

However, there are some FTP where you can use a "guest". The name for this user is "anonymous" and you don't need a password.

![](/assets/images/anon.png)




