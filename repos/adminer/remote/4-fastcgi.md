## `adminer:4-fastcgi`

```console
$ docker pull adminer@sha256:5e969bae1d530db7e07166a4c863f04a41fd29b16c425d901c9cc30d9ae80c2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `adminer:4-fastcgi` - linux; amd64

```console
$ docker pull adminer@sha256:c58df4818a9fa95adf60d8069da5f8c1c8e83030b07576e642e66cc80e466f3f
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31416023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375fadd8aed819eaa90b87532efb39fcb11cc0b705cb96fcc863cea46680a4e1`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 03 Nov 2017 22:10:25 GMT
ADD file:90342832e4e7931e42954849ed51216e77b3c974270ed83e9da5648918fb5e66 in / 
# Fri, 03 Nov 2017 22:10:25 GMT
CMD ["/bin/sh"]
# Sat, 04 Nov 2017 10:30:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pcre-dev 		pkgconf 		re2c
# Sat, 04 Nov 2017 10:30:51 GMT
RUN apk add --no-cache --virtual .persistent-deps 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 04 Nov 2017 10:30:52 GMT
RUN set -x 	&& addgroup -g 82 -S www-data 	&& adduser -u 82 -D -S -G www-data www-data
# Sat, 04 Nov 2017 10:30:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 04 Nov 2017 10:30:53 GMT
RUN mkdir -p $PHP_INI_DIR/conf.d
# Sat, 04 Nov 2017 10:35:58 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data
# Sat, 04 Nov 2017 10:35:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Sat, 04 Nov 2017 10:35:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Sat, 04 Nov 2017 10:35:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 04 Nov 2017 11:09:15 GMT
ENV GPG_KEYS=1A4E8B7277C42E53DBA9C7B9BCAA30EA9C0D5763 6E4F6AB321FDC07F2C332E3AC2BF0BC433CFC8B3
# Sat, 04 Nov 2017 11:09:15 GMT
ENV PHP_VERSION=7.0.25
# Sat, 04 Nov 2017 11:09:15 GMT
ENV PHP_URL=https://secure.php.net/get/php-7.0.25.tar.xz/from/this/mirror PHP_ASC_URL=https://secure.php.net/get/php-7.0.25.tar.xz.asc/from/this/mirror
# Sat, 04 Nov 2017 11:09:15 GMT
ENV PHP_SHA256=5cc14bd20fb2226f6d34465662425cd100441bde9042ea1cef2e4506d6ded8cc PHP_MD5=
# Sat, 04 Nov 2017 11:09:33 GMT
RUN set -xe; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		mkdir -p /usr/src; 	cd /usr/src; 		wget -O php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		wget -O php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del .fetch-deps
# Sat, 04 Nov 2017 11:09:33 GMT
COPY file:207c686e3fed4f71f8a7b245d8dcae9c9048d276a326d82b553c12a90af0c0ca in /usr/local/bin/ 
# Sat, 04 Nov 2017 11:13:50 GMT
RUN set -xe 	&& apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		coreutils 		curl-dev 		libedit-dev 		openssl-dev 		libxml2-dev 		sqlite-dev 		&& export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	&& docker-php-source extract 	&& cd /usr/src/php 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--disable-cgi 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pcre-regex=/usr 				$PHP_EXTRA_CONFIGURE_ARGS 	&& make -j "$(nproc)" 	&& make install 	&& { find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; } 	&& make clean 	&& cd / 	&& docker-php-source delete 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-cache --virtual .php-rundeps $runDeps 		&& apk del .build-deps 		&& pecl update-channels 	&& rm -rf /tmp/pear ~/.pearrc
# Sat, 04 Nov 2017 11:13:50 GMT
COPY multi:3a3ce8aa3891c64454909e9f8257446a1817abe660b49a7baaa26f28bfdc444d in /usr/local/bin/ 
# Sat, 04 Nov 2017 11:13:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 04 Nov 2017 11:13:51 GMT
WORKDIR /var/www/html
# Sat, 04 Nov 2017 11:13:51 GMT
RUN set -ex 	&& cd /usr/local/etc 	&& if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi 	&& { 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf 	&& { 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = [::]:9000'; 	} | tee php-fpm.d/zz-docker.conf
# Sat, 04 Nov 2017 11:13:52 GMT
EXPOSE 9000/tcp
# Sat, 04 Nov 2017 11:13:52 GMT
CMD ["php-fpm"]
# Sat, 04 Nov 2017 15:55:30 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 04 Nov 2017 15:55:33 GMT
RUN apk add --no-cache libpq
# Sat, 04 Nov 2017 15:55:54 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Sat, 04 Nov 2017 15:55:55 GMT
COPY multi:515cdb7e8ed0278965e56c4b579e89987c42be4b42a309c70682464e9c9451c5 in /var/www/html/ 
# Sat, 04 Nov 2017 15:55:55 GMT
ENV ADMINER_VERSION=4.3.1
# Sat, 04 Nov 2017 15:55:55 GMT
ENV ADMINER_DOWNLOAD_SHA256=71688c5db4d4e504c48c26ec2966ad85e721ef61e0377c5505cfb50b026d5491
# Sat, 04 Nov 2017 15:55:55 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=fd016c93bb3bb8e85ed9cf826064584012c4db83f30c4948d701250e29a6d953
# Sat, 04 Nov 2017 15:55:57 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION-en.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Sat, 04 Nov 2017 15:55:58 GMT
COPY file:7d0b9a0787be28f6522891c0b9e7249e1c7d88759916642b95d9d3296ed72be5 in /usr/local/bin/ 
# Sat, 04 Nov 2017 15:55:58 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 04 Nov 2017 15:55:58 GMT
USER [adminer]
# Sat, 04 Nov 2017 15:55:58 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:49388a8c9c86a6f56d228954eede699c64fce6c671a989e3e21c391859694645`  
		Last Modified: Wed, 25 Oct 2017 23:22:36 GMT  
		Size: 2.4 MB (2385012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e5f7c337501eeff98e19cc2d10f4c50fd8bfcce7fe2640fa219b410b1cc2676`  
		Last Modified: Sat, 04 Nov 2017 11:58:11 GMT  
		Size: 1.3 MB (1308940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2765a1878d4da8aa3135f8e56cfa7e36daa2a263efa8fd09357aba95f6535a98`  
		Last Modified: Sat, 04 Nov 2017 11:58:09 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95785b88ca8822903609d4912df09c6ae0866313da1f6cfeb3a68b0d3bf2a14f`  
		Last Modified: Sat, 04 Nov 2017 11:58:08 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdef5322e2a9b217da5b1fdc9d6f158c7e7cb6dabceb39d99836d4b861b02136`  
		Last Modified: Sat, 04 Nov 2017 12:04:46 GMT  
		Size: 12.0 MB (11982284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01f0d25e4cc41ed07f9e0249e0f5b13901182e05d61a4ef9c3cb803cd9843317`  
		Last Modified: Sat, 04 Nov 2017 12:04:42 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:075c3d94225d5379d3074ec87d8a77c7b2f031b3075075bec9aa4e4ff818d8ee`  
		Last Modified: Sat, 04 Nov 2017 12:04:50 GMT  
		Size: 14.1 MB (14074629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d33fa34d984b3b5aed43f484dc0ab386e3cb2c9588b5cb8bd9325c393c81c15`  
		Last Modified: Sat, 04 Nov 2017 12:04:42 GMT  
		Size: 2.2 KB (2159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a88480204f09f3d11e87281615ead694f71a4208f83c76032ebb4288cbabe9e`  
		Last Modified: Sat, 04 Nov 2017 12:04:43 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:569e6e7b3d9d95983784da1076396104e4741a6e669225374dfbbb58f2909f38`  
		Last Modified: Sat, 04 Nov 2017 12:04:42 GMT  
		Size: 7.7 KB (7661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63c23e01e016d26faf7843108dbed5aaddf6233878fa40ee1d04a17e914c2906`  
		Last Modified: Sat, 04 Nov 2017 15:57:32 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837e1c851b77861cb70c549cf02b8b50f6b0a07c90aa05358a5af51956595c3d`  
		Last Modified: Sat, 04 Nov 2017 15:57:29 GMT  
		Size: 1.2 MB (1211372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a2f58658043c2ddc641bbd222397a117100832c672bfc946eeaeabe44fe411c`  
		Last Modified: Sat, 04 Nov 2017 15:57:29 GMT  
		Size: 119.5 KB (119478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5591b1c6b4c8a726ebafe530969563a4bc4a4d51720ecf3106a26336b69e5e`  
		Last Modified: Sat, 04 Nov 2017 15:57:29 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672a9911bbfb049b50d65261532e899ac0cccf552f8a52b9985174e7c1d843af`  
		Last Modified: Sat, 04 Nov 2017 15:57:29 GMT  
		Size: 319.1 KB (319106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a67190da8483ad253098974165134bbeb7e01efd1e44c4a94acc724be044ed1`  
		Last Modified: Sat, 04 Nov 2017 15:57:29 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
