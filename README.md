# A Fork of Nginx ReverseProxy Creator by bilyboy785
![NginxLogo](https://www.nginx.com/resources/wiki/_static/img/logo.png)

# Updates/changes
* Changed from apt-get to yum for use on centos
* you can now enter your IP:port rather than just a port!
* changed service nginx stop/start to systemctl 


## Original Documentation follows
Just a little script to create Nginx reverse proxy with SSL support. Simply run the script with or without parameters and that's all !

## Installation
To start, just clone this repo to your **/opt** folder :
```
git clone https://github.com/bilyboy785/nginx-reverseproxy-creator.git /opt/nginxreverse && cd /opt/nginxreverse
```

## Defaut Usage
By default, you can launch the script without parameters :
```
./nginx-reverse.sh
```

It will ask you some informations about domain and application port :

![NginxReverse](https://goo.gl/W3NNUf)

## Advanced Usage
You can use parameters when launching the script. Two options are available :
 * **classic** : create a classic reverse proxy with HTTP support (80)
 * **ssl** : create an SSL reverse proxy with HTTPS (443) and auto redirection from 80 to 443
 
### Classic Option
If you choose classic option, here an example :
```
./nginx-reverse.sh classic app.domain.tld 8888
```
 
### SSL Option
If you choose SSL reverse, you need to add your email and RSA Key Size, like this :
```
./nginx-reverse.sh ssl app.domain.tld 8888 contact@domain.tld 2048
```
