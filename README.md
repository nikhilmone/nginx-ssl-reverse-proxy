# nginx-ssl-reverse-proxy

This is a very minimalistic reverse-proxy setup with SSL.

### Create a certificate and key using below command. Set env variables in advance:

```
sudo openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout $private_dir/nginx-selfsigned.key -out $cert_dir/nginx-selfsigned.crt
```

Keep the certificate generated in the [certs](https://github.com/nikhilmone/nginx-ssl-reverse-proxy/tree/master/setup/nginx/certs) directory and the key generated in [private](https://github.com/nikhilmone/nginx-ssl-reverse-proxy/tree/master/setup/nginx/private) directory.

### The actual setup goes here:

[NGINX configuration file](https://github.com/nikhilmone/nginx-ssl-reverse-proxy/blob/master/setup/nginx/conf.d/default.conf)

### A working front-end with SSL and reverse proxy running on port 443:

![](https://github.com/nikhilmone/nginx-ssl-reverse-proxy/blob/master/screenshots/frontend.png)

### Working backends on HTTP:

##### Backend 1 running on port 8090:

![](https://github.com/nikhilmone/nginx-ssl-reverse-proxy/blob/master/screenshots/backend1.png)

##### Backend 2 running on port 8095:

![](https://github.com/nikhilmone/nginx-ssl-reverse-proxy/blob/master/screenshots/backend2.png)

# Reverse proxy in action for backends:

##### Backend 1 through reverse-proxy over HTTPS:

![](https://github.com/nikhilmone/nginx-ssl-reverse-proxy/blob/master/screenshots/backend1_https.png)

##### Backend 2 through reverse-proxy over HTTPS:

![](https://github.com/nikhilmone/nginx-ssl-reverse-proxy/blob/master/screenshots/backend2_https.png)
