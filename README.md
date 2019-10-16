# nginx-ssl-reverse-proxy

```
sudo openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout $private_dir/nginx-selfsigned.key -out $cert_dir/nginx-selfsigned.crt
```

### A working front-end with SSL and reverse proxy:

[Front End](https://github.com/nikhilmone/nginx-ssl-reverse-proxy/blob/master/frontend.png)
