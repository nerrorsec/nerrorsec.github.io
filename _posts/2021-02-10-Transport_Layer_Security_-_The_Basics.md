---
layout: post
title: "Transport Layer Security - The Basics"
categories:
  - Blog
tags:
  - tls, ssl
last_modified_at: 2021-02-10
---

Transport Layer Security (TLS) is the successor protocol to SSL that establishes an encrypted session between two computers on the Internet. TLS/SSL certificates are the backbone of internet security and it is what keeps our information safe while online. It encrypts and decrypts information between the client and the server while communicating with websites making sensitive information like banking details, account credentials, etc. inaccessible to any eavesdropper or any party between the client and the server. With the increasing use of personal and other critical data on the internet and actions like banking and shopping online, SSL has undergone multiple revisions to improve security and to mitigate attacks.

### How do you get an SSL/TLS certificate? 
Website owners can obtain certificates from a certificate authority that is responsible for issuing the certificates. The certificate authorities validates if the identity of the site you are interacting with is authentic and the certificate issued can confirm the domain and verify their identity. While anyone can create a certificate, browsers only trust certificates that come from an organization on their pre-installed list of trusted CAs. They can then install the certificate in their web server to implement it in their website. Use of an SSL certificate in a website can be verified with https:// at the start of the domain name in the URL bar and a padlock symbol in today’s browsers. 

### Workflow

![How SSL works](https://github.com/nerrorsec/nerrorsec.github.io/blob/master/assets/images/posts/Transport-Layer-Security/How-SSL-Works.png)

Here, when you visit a website with SSL/TLS certificate installed, the browser sends a request to the server. The server responds with its SSL/TLS certificate including a public key. The browser then, checks the certificate and verifies if it the certificate has expired, been revoked and that it is communicating to the intended party and not an impostor. 

If the browser trusts the certificate, it creates, encrypts, and sends back a symmetric session key using the server’s public key. The server decrypts the symmetric session key using its private key and sends back an acknowledgement encrypted with the session key to start the encrypted session. The private key is available to the server only meaning no one else can read the message sent by the browser. 

Now, the browser and the server encrypt all transmitted data with the session key. 

### What should you use SSL or TLS? 
“Although the terms SSL and TLS are often used interchangeably, it is important to note that all SSL versions are deprecated due to numerous security vulnerabilities and all web servers should only be using TLS.” The latest TLS version available is TLS 1.3. 

### Checking SSL/TLS certificates 
A small portion of details of the certificate can be viewed in the browser by clicking the padlock icon and visiting ‘More Information’ and ‘Security’ tab. Also, there are numerous online tools to check SSL/TLS certificates like [SSL Labs](https://www.ssllabs.com/), [SSL Checker](https://www.thesslstore.com/ssltools/ssl-checker.php), [Geekflare](https://gf.dev/tls-test), and more. 
