---
layout: "post"
title: "Bypass SSL Pinning IOS "
date: 2024-04-26T21:44:02+01:00
---
> <html><body><b><p style="color:#ffffff;font-size:25px">Introduction :</p></b></body></html>

Always in bypassing SSL certificates, most rely on well-known Apps in both systems (iPhone, Android). However, these Apps depend on well-known libraries which they use to bypass the certificate. Here are some sources that can be useful for delving deeper into the topic:

Explanation of how the NSURLSession library works:
```sh
https://developer.apple.com/documentation/foundation/nsurlsession
```
Example of bypassing the library from one of the Applactions:
```sh
https://nabla-c0d3.github.io/blog/2019/05/18/ssl-kill-switch-for-ios12
```


> <html><body><b><p style="color:#ffffff;font-size:25px">Why SSL Kill switch usless ?:</p></b></body></html>

Most of the time, the SSL Kill Switch tweak and Frida are useless for many reasons, One of which is that some iOS applications use custom SSL certificates. So, how can we bypass SSL pinning in iOS apps without using SSL Kill Switch, Frida, or reverse engineering? There is a way, and that will be our topic .

> <html><body><b><p style="color:#ffffff;font-size:25px">Downgrade IOS apps </p></b></body></html>

My favorite technique to bypass jailbreak detection and SSL pinning is downgrading. Let's see how downgrading can be a good way to bypass these restrictions. I tried using SSL Kill Switch but it not work ! :

<img src="/img/1.png" alt="centered image" />

How can we downgrade an iOS app? You need three things to achieve that:

- Jailbreak for iOS 15/16
- TrollStore
- AppStore++

To download AppStore++ from here:
```sh
https://github.com/CokePokes/AppStorePlus-TrollStore
```
After you have all of these set up, just go to AppStore++ and follow the steps :

1- First go to AppStore++ :

<img src="/img/01.png" alt="centered image" />

2- Hold on the app you want to downgrade. In our case, it's Instagram. Also, we see the current version is (327.1.6). Click on the 'Downgrade' tab  :

<img src="/img/02.png" alt="centered image" />

3- You will see a list of all Instagram versions. Choose any version you want. In my case, I chose (328.1.3):

<img src="/img/03.png" alt="centered image" />

4- As you can see, I am able to change the Instagram version:

<img src="/img/04.png" alt="centered image" />

> <html><body><b><p style="color:#6d0000;font-size:25px">Reference & Answers:</p></b></body></html>

Does downgrading work every time?

No, but it's a good way to bypass SSL pinning 

> <html><body><b><p style="color:#6d0000;font-size:25px">Author:</p></b></body></html>

If you want to copy anything from these articles, please don't forget to give credit. :)

**Twitter** :

```
https://twitter.com/xcode0x
```

**linkedin** :
```sh
https://www.linkedin.com/in/mohamed-a-52389b252/
```
