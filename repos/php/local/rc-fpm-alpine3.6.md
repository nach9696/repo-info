# `php:7.2.0RC5-fpm-alpine3.6`

## Docker Metadata

- Image ID: `sha256:1a951a6d67c9efa4b8aa8f38dc38328268121611918dc931eefe250f0fd50a82`
- Created: `2017-11-04T10:05:10.501151839Z`
- Virtual Size: ~ 75.56 Mb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Entrypoint: `["docker-php-entrypoint"]`
- Command: `["php-fpm"]`
- Environment:
  - `PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`
  - `PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pcre-dev 		pkgconf 		re2c`
  - `PHP_INI_DIR=/usr/local/etc/php`
  - `PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data`
  - `PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2`
  - `PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2`
  - `PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie`
  - `GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F`
  - `PHP_VERSION=7.2.0RC5`
  - `PHP_URL=https://downloads.php.net/~pollita/php-7.2.0RC5.tar.xz`
  - `PHP_ASC_URL=https://downloads.php.net/~pollita/php-7.2.0RC5.tar.xz.asc`
  - `PHP_SHA256=92a745048912beb3f6c2a3c188ce695a51852c67201fdf9a21dafe59f51aecc1`
  - `PHP_MD5=`
