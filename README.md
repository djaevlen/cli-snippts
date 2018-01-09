# cli-snippts
Collection of CLI snippets


### Pack a folder to a tar file. Without compression
`tar cvf myfolder.tar myfolder`


### Extract a tar file. Without compression
`tar -xvf file.tar`

### Test NGINX before restart
`sudo nginx -c /etc/nginx/nginx.conf -t`

### Restart NGINX
`sudo /etc/init.d/nginx restart`

### Create SSL cert for localhost ###
`openssl req \
    -newkey rsa:2048 \
    -x509 \
    -nodes \
    -keyout server.pem \
    -new \
    -out server.pem \
    -subj /CN=localhost \
    -reqexts SAN \
    -extensions SAN \
    -config <(cat /System/Library/OpenSSL/openssl.cnf \
        <(printf '[SAN]\nsubjectAltName=DNS:localhost')) \
    -sha256 \
    -days 365
`
