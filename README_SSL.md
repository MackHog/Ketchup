# SSL

## Create SSL cert
### Option 1
#### Install
Install opensll

#### Generate Cert
Run openssl
Go to C:\Program Files\OpenSSL-Win64\bin and run opensll as admin

#### Create private and public key
openssl req -x509 -newkey rsa:4096 -keyout private_helpcenterapi.pem -out public_cert_helpcenterapi.pem -days 365

#### Create pfx file
openssl pkcs12 -export -in public_cert_helpcenterapi.pem -inkey private_helpcenterapi.pem -out helpcenter_clientauthentication.pfx

### Option 2
#### Use mkcert
To create certs and install the trusted CA for localhost use https://github.com/FiloSottile/mkcert 

#### Install mkcert then
mkcert localhost 127.0.0.1

#### Trust the CA by
mkcert -install

### done
That is all, now use the cert in your local env project.