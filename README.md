
## Table of Contents
- [Setup](#setup)
  - [Install Nginx](#install-nginx)
  - [Check Nginx config path](#check-nginx-config-path)
  - [Overide the nginx.conf file](#overide-the-nginxconf-file)
  - [Generate self-signed certificate](#generate-self-signed-certificate)
  - [Reference](#reference)
## Setup
- MacOS
- 

### Install Nginx
```bash
brew install nginx && nginx -v
```

### Check Nginx config path
```bash
nginx -V
```
![alt text](images/nginx-conf.png)
👉 /opt/homebrew/etc/nginx/nginx.conf

### Overide the nginx.conf file
```bash
cat nginx.conf >  /opt/homebrew/etc/nginx/nginx.conf
```

### Generate self-signed certificate
```bash
mkdir nginx-certs &&
cd nginx-certs &&
openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout nginx-selfsigned.key -out nginx-selfsigned.crt
```

Enter some basic information of the certificate that promted
![alt text](images/gen-cert.png)

### Reference
[![Tutorial](https://img.icons8.com/color/48/000000/youtube-play.png)](https://www.youtube.com/watch?v=q8OleYuqntY)
[![Source](https://img.icons8.com/color/48/000000/gitlab.png)](https://gitlab.com/twn-youtube/nginx-crash-course)