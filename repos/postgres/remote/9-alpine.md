## `postgres:9-alpine`

```console
$ docker pull postgres@sha256:bafac9478d8cca8965d091ee228c6897bfa0e2ad4704c26f58bedc8b37c4cde1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `postgres:9-alpine` - linux; amd64

```console
$ docker pull postgres@sha256:e580c1eac7e4af5bbf7233c35bc871b349884b54ae0cb1d768977343f9c770fe
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14685695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45bb1b42de29d71a45eb9615d8838a88ed1bc9187395c48d720c34c7aed6cc97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 03 Nov 2017 22:10:27 GMT
ADD file:92bfed3f8dfbee01eab85c6a1d6bc6894c5a75f9a4e2c414e9b4d05b9fcd19d0 in / 
# Fri, 03 Nov 2017 22:10:27 GMT
CMD ["/bin/sh"]
# Sat, 04 Nov 2017 09:10:49 GMT
RUN set -ex; 	postgresHome="$(getent passwd postgres)"; 	postgresHome="$(echo "$postgresHome" | cut -d: -f6)"; 	[ "$postgresHome" = '/var/lib/postgresql' ]; 	mkdir -p "$postgresHome"; 	chown -R postgres:postgres "$postgresHome"
# Sat, 04 Nov 2017 09:10:49 GMT
ENV LANG=en_US.utf8
# Sat, 04 Nov 2017 09:10:50 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 04 Nov 2017 09:10:50 GMT
ENV PG_MAJOR=9.6
# Sat, 04 Nov 2017 09:10:50 GMT
ENV PG_VERSION=9.6.5
# Sat, 04 Nov 2017 09:10:50 GMT
ENV PG_SHA256=06da12a7e3dddeb803962af8309fa06da9d6989f49e22865335f0a14bad0744c
# Sat, 04 Nov 2017 09:13:25 GMT
RUN set -ex 		&& apk add --no-cache --virtual .fetch-deps 		ca-certificates 		openssl 		tar 		&& wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2" 	&& echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c - 	&& mkdir -p /usr/src/postgresql 	&& tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	&& rm postgresql.tar.bz2 		&& apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		make 		openssl-dev 		perl 		perl-ipc-run 		util-linux-dev 		zlib-dev 		&& cd /usr/src/postgresql 	&& awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new 	&& grep '/var/run/postgresql' src/include/pg_config_manual.h.new 	&& mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb' 	&& wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb' 	&& ./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 	&& make -j "$(nproc)" world 	&& make install-world 	&& make -C contrib install 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	&& apk del .fetch-deps .build-deps 	&& cd / 	&& rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	&& find /usr/local -name '*.a' -delete
# Sat, 04 Nov 2017 09:13:27 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Sat, 04 Nov 2017 09:13:27 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Sat, 04 Nov 2017 09:13:27 GMT
ENV PGDATA=/var/lib/postgresql/data
# Sat, 04 Nov 2017 09:13:28 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA" # this 777 will be replaced by 700 at runtime (allows semi-arbitrary "--user" values)
# Sat, 04 Nov 2017 09:13:28 GMT
VOLUME [/var/lib/postgresql/data]
# Sat, 04 Nov 2017 09:13:29 GMT
COPY file:d5038a27fbcfa2f7c3a5e92ffdbfda1676a7a65ecb52a9b377a6041a59e1c1d7 in /usr/local/bin/ 
# Sat, 04 Nov 2017 09:13:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 04 Nov 2017 09:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 04 Nov 2017 09:13:30 GMT
EXPOSE 5432/tcp
# Sat, 04 Nov 2017 09:13:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b1f00a6a160cd3696edba6f13ebd1d6a5808216a78ec4b753444ab8f30483b1f`  
		Last Modified: Wed, 25 Oct 2017 23:22:48 GMT  
		Size: 2.0 MB (1970236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a88a2feda9fd9c11a4e26126bdb3c7b35e03f06fc60232e8146ab66c6e3fbe`  
		Last Modified: Sat, 04 Nov 2017 09:26:35 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd866a92fb72cb1d8102afcef8d01e8751f657b317d150bfaa34a8fe61b2f11`  
		Last Modified: Sat, 04 Nov 2017 09:26:35 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c43cb896f3eb33c7efa88366a303852b531056660de4fcad03146e987e62de9`  
		Last Modified: Sat, 04 Nov 2017 09:26:38 GMT  
		Size: 12.7 MB (12705880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341573b3bdddd98950797e966522dbd5f3d0746023f5eaaa96f73f21ec326251`  
		Last Modified: Sat, 04 Nov 2017 09:26:33 GMT  
		Size: 7.1 KB (7072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7ccfa970786512c79ca433de88cc4d3155631d4d5b96e7d475ba9f0cc939193`  
		Last Modified: Sat, 04 Nov 2017 09:26:33 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d28928466b83df54728e82cd4e81a4fa7e6e25d733f520a5eacc0a0074f471`  
		Last Modified: Sat, 04 Nov 2017 09:26:33 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b424957445a51466945fe475cd40420f2ea87c46cafed2b779ce45cbabde140`  
		Last Modified: Sat, 04 Nov 2017 09:26:33 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c1161620fbecf8fcbafe1f0d42f56a0152db77f93d15f61e958cc9b2e9f888`  
		Last Modified: Sat, 04 Nov 2017 09:26:34 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
