## Instuction for setup docker registry on local machine

Local domain name: registry.local
Add it to /etc/hosts file

```bash
sudo echo "127.0.0.1 registry.local" >> /etc/hosts
```

Generate ssl sertificaties with [mkcert](https://github.com/FiloSottile/mkcert). 
```bash
mkdir certs
mkcert -key-file certs/key.pem -cert-file cert.pem registry.local *.registry.local
```

Run docker-compose

```bash
docker-compose up -d
```

Open https://registry.local in browser.
