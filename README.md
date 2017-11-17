Sylius Shop Api Demo
===

local demo shop with cutting edge shop api

install
---

```
$ git clone https://github.com/sdleiw/SyliusApi
$ cd SyliusApi
$ composer install
$ bin/console sylius:install
$ bin/console server:start
$ open http://localhost:8000/
```

config
---

Generate the SSH keys for JWTAuthenticationBundle:

```
$ mkdir -p var/jwt # For Symfony3+, no need of the -p option
$ openssl genrsa -out var/jwt/private.pem -aes256 4096
$ openssl rsa -pubout -in var/jwt/private.pem -out var/jwt/public.pem
```

set `account_verification_required = 0` in the `sylius_channel` table, 
register with verification is currently not supported
