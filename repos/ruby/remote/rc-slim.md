## `ruby:rc-slim`

```console
$ docker pull ruby@sha256:2c442167eba97ffbd83fed417d2b6a12d889a31dd6089f48bcba77222ebc117e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ruby:rc-slim` - linux; amd64

```console
$ docker pull ruby@sha256:0486ad0e56710fbc971bb5a76ef7b264a48fac392381479403a60f25afc7bcdc
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83461466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46ae60662fe132fbbe87846f84e692ec29068e51dc46c6a3f6df896f59fdd5ab`
-	Default Command: `["irb"]`

```dockerfile
# Sat, 04 Nov 2017 05:26:40 GMT
ADD file:a71e077a42995a68ffe4834d85cfe26af4ea12aa8ed43decc03cc487124b1f70 in / 
# Sat, 04 Nov 2017 05:26:40 GMT
CMD ["bash"]
# Sat, 04 Nov 2017 05:41:11 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Nov 2017 05:41:12 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 04 Nov 2017 05:41:12 GMT
ENV RUBY_MAJOR=2.5-rc
# Sat, 04 Nov 2017 05:41:12 GMT
ENV RUBY_VERSION=2.5.0-preview1
# Sat, 04 Nov 2017 05:41:12 GMT
ENV RUBY_DOWNLOAD_SHA256=c2f518eb04b38bdd562ba5611abd2521248a1608fc466368563dd794ddeddd09
# Sat, 04 Nov 2017 05:41:12 GMT
ENV RUBYGEMS_VERSION=2.7.0
# Sat, 04 Nov 2017 05:41:13 GMT
ENV BUNDLER_VERSION=1.16.0
# Sat, 04 Nov 2017 05:44:01 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force
# Sat, 04 Nov 2017 05:44:02 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 04 Nov 2017 05:44:02 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 04 Nov 2017 05:44:02 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Nov 2017 05:44:02 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sat, 04 Nov 2017 05:44:03 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:3e17c6eae66cd23c59751c8d8f5eaf7044e0611dc5cebb12b1273be07cdac242`  
		Last Modified: Mon, 09 Oct 2017 21:41:38 GMT  
		Size: 45.1 MB (45129088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab85ecbee58cc2f65cbdd9d37ebe0a85aeb86fc879d742853a84b6e0ba00b79`  
		Last Modified: Sat, 04 Nov 2017 06:27:44 GMT  
		Size: 12.8 MB (12772167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73bce7636b76167772be687f2627651c224ad3b78298eb5c045598609f7601ba`  
		Last Modified: Sat, 04 Nov 2017 06:27:41 GMT  
		Size: 206.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289d5ecb0824c2b0d9b902ea63a60a95282b3fb74fb33c32bb8a0c043e8e3fd9`  
		Last Modified: Sat, 04 Nov 2017 06:27:47 GMT  
		Size: 25.6 MB (25559841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d86f45418d0698407b5e6ab9388b1db025e2fa1c90420279d666f29ab5169f`  
		Last Modified: Sat, 04 Nov 2017 06:27:41 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:rc-slim` - linux; arm variant v5

```console
$ docker pull ruby@sha256:ffaa83fd2e78c332217c1461d40bd371f62f3a6cf4c8c83f0fd971cf91ec4390
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.3 MB (80262832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c111e3964b8e691e7e78de02b27c6e96eedbe191a617c8d40b060eb1562ee20c`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 09 Oct 2017 21:44:33 GMT
ADD file:faa50a4d3491f148f07964f6b9f9c8e97c0cf64588b20deb10f24e2f4f6c6b87 in / 
# Mon, 09 Oct 2017 21:44:33 GMT
CMD ["bash"]
# Tue, 10 Oct 2017 00:31:11 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 10 Oct 2017 00:31:13 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 26 Oct 2017 01:24:10 GMT
ENV RUBY_MAJOR=2.5-rc
# Thu, 26 Oct 2017 01:24:11 GMT
ENV RUBY_VERSION=2.5.0-preview1
# Thu, 26 Oct 2017 01:24:11 GMT
ENV RUBY_DOWNLOAD_SHA256=c2f518eb04b38bdd562ba5611abd2521248a1608fc466368563dd794ddeddd09
# Sat, 04 Nov 2017 01:24:20 GMT
ENV RUBYGEMS_VERSION=2.7.0
# Sat, 04 Nov 2017 01:24:20 GMT
ENV BUNDLER_VERSION=1.16.0
# Sat, 04 Nov 2017 01:27:19 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force
# Sat, 04 Nov 2017 01:27:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 04 Nov 2017 01:27:20 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 04 Nov 2017 01:27:20 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Nov 2017 01:27:21 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sat, 04 Nov 2017 01:27:22 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:3c60e7fc5441d6c90edac385048cfe55b732e74ac7a95ce0f52555d1fdd4777a`  
		Last Modified: Mon, 09 Oct 2017 21:50:32 GMT  
		Size: 43.8 MB (43815910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c416c81ba4dff87a2abaab346993bdf7c88b658e2b24bcaf567a01d8bb5f24`  
		Last Modified: Tue, 10 Oct 2017 01:12:44 GMT  
		Size: 11.3 MB (11337171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda218d8320c952835d12b60c05b0a2a04808648848698c2458108f65d88a019`  
		Last Modified: Tue, 10 Oct 2017 01:12:40 GMT  
		Size: 206.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4c8ad49beb46300143ad5c5773af463b89d4725b7a70b75537425f58207d019`  
		Last Modified: Sat, 04 Nov 2017 02:10:44 GMT  
		Size: 25.1 MB (25109350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96758929c89f09c9597599445ecb60fb3bd9878aaeb0f32d9bd1d74c0fc9e008`  
		Last Modified: Sat, 04 Nov 2017 02:10:36 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:rc-slim` - linux; arm variant v7

```console
$ docker pull ruby@sha256:46077c5f20e4dd3ace8c33539bb7770b21e0a1d0d33471b7eb764c40ae729a11
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77617037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8b287c32fea5d6f950cf02f37849f1cdd48ba71c783232b6ddaf37e1ea5eb1`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 09 Oct 2017 21:45:23 GMT
ADD file:8b7cf813a113aa20eb7f5eecbb602ff5d306b7586add13ed5e082cd09770edb4 in / 
# Mon, 09 Oct 2017 21:45:23 GMT
CMD ["bash"]
# Tue, 10 Oct 2017 00:22:14 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 10 Oct 2017 00:22:18 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 26 Oct 2017 01:14:08 GMT
ENV RUBY_MAJOR=2.5-rc
# Thu, 26 Oct 2017 01:14:08 GMT
ENV RUBY_VERSION=2.5.0-preview1
# Thu, 26 Oct 2017 01:14:08 GMT
ENV RUBY_DOWNLOAD_SHA256=c2f518eb04b38bdd562ba5611abd2521248a1608fc466368563dd794ddeddd09
# Sat, 04 Nov 2017 01:14:17 GMT
ENV RUBYGEMS_VERSION=2.7.0
# Sat, 04 Nov 2017 01:14:18 GMT
ENV BUNDLER_VERSION=1.16.0
# Sat, 04 Nov 2017 01:16:43 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force
# Sat, 04 Nov 2017 01:16:43 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 04 Nov 2017 01:16:43 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 04 Nov 2017 01:16:43 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Nov 2017 01:16:44 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sat, 04 Nov 2017 01:16:44 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0d9fbbfaa2cd8961ae50e51e7388e3a2a1a5ca2c105389b56a3a862dfe76d035`  
		Last Modified: Mon, 09 Oct 2017 21:52:12 GMT  
		Size: 41.8 MB (41841946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d35a2c00091285c2fc2ebb932b11b45eb5b4bb3ef250f293ad54ba7094577bc4`  
		Last Modified: Tue, 10 Oct 2017 01:01:12 GMT  
		Size: 10.9 MB (10857369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb7bf878e9c07e0b88216d82ef5f9b41183e1ea0d9051ecb47d6ff5258aca7c`  
		Last Modified: Tue, 10 Oct 2017 01:01:08 GMT  
		Size: 206.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff8c0d10865e55826291d7ac887c20280b695dcfd54911f7bae53edd33d5182`  
		Last Modified: Sat, 04 Nov 2017 01:58:02 GMT  
		Size: 24.9 MB (24917321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:831af9df0288f8635f37f94a8204aea1fbd586faa976435ad87dd177045306be`  
		Last Modified: Sat, 04 Nov 2017 01:57:56 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:rc-slim` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:db056ecfc6245b121f2624af3d51834e1bbb4fb50d8ba17e32056f48159d2089
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79826497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:189e5e39e4f9cb185fe0ae81eb720febf34c23237bdec2126f7d5bd7bdc8e1a1`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 09 Oct 2017 21:47:18 GMT
ADD file:bf097edec8505e5cb1e432319988aeb28a6f918edef706b3c543fa61aaaea4cb in / 
# Mon, 09 Oct 2017 21:47:19 GMT
CMD ["bash"]
# Tue, 10 Oct 2017 07:21:11 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 10 Oct 2017 07:21:13 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 25 Oct 2017 20:44:00 GMT
ENV RUBY_MAJOR=2.5-rc
# Wed, 25 Oct 2017 20:44:00 GMT
ENV RUBY_VERSION=2.5.0-preview1
# Wed, 25 Oct 2017 20:44:01 GMT
ENV RUBY_DOWNLOAD_SHA256=c2f518eb04b38bdd562ba5611abd2521248a1608fc466368563dd794ddeddd09
# Sat, 04 Nov 2017 16:22:47 GMT
ENV RUBYGEMS_VERSION=2.7.0
# Sat, 04 Nov 2017 16:22:47 GMT
ENV BUNDLER_VERSION=1.16.0
# Sat, 04 Nov 2017 16:31:38 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force
# Sat, 04 Nov 2017 16:31:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 04 Nov 2017 16:31:46 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 04 Nov 2017 16:31:49 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Nov 2017 16:31:56 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sat, 04 Nov 2017 16:31:58 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0e5a8be23912597ff0d89db096abd4c4383c8cf4ee700d333b86f881ea289875`  
		Last Modified: Mon, 09 Oct 2017 22:01:04 GMT  
		Size: 42.9 MB (42911727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd4518c9184ff3fe2631b80187dc1942b528822ee88624b0e0232ea19772de94`  
		Last Modified: Tue, 10 Oct 2017 08:38:44 GMT  
		Size: 11.6 MB (11580911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1815da5c8d1101ac2ff3e23fd627a2c38f22de9cd2096e71e4abab845933af`  
		Last Modified: Tue, 10 Oct 2017 08:38:27 GMT  
		Size: 205.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a42c3e075b2dcb684eff36e5a6dbd893f0981559b9da57f55c8e5976cb1315`  
		Last Modified: Sat, 04 Nov 2017 18:10:16 GMT  
		Size: 25.3 MB (25333490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1fa177f8d7d78fb1d9262a9dd90583e13e600ed607a8761bfdb5d4437ba128c`  
		Last Modified: Sat, 04 Nov 2017 18:10:07 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:rc-slim` - linux; 386

```console
$ docker pull ruby@sha256:63145624d8f288a104b7306d37f6aa689aa360aedcd46a59f5e4659b8d0ecfdb
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.2 MB (87207881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a2d6de021466056757b387d7cbb4f50407924417b9d0e307285bd6cdbdf2148`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 09 Oct 2017 21:45:21 GMT
ADD file:14ce0e7f11224a3d3ef5a62ece43529a687ada430b8d8ecfa0e0a5d2d1e47467 in / 
# Mon, 09 Oct 2017 21:45:21 GMT
CMD ["bash"]
# Tue, 10 Oct 2017 02:36:59 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 10 Oct 2017 02:37:00 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 26 Oct 2017 02:43:20 GMT
ENV RUBY_MAJOR=2.5-rc
# Thu, 26 Oct 2017 02:43:20 GMT
ENV RUBY_VERSION=2.5.0-preview1
# Thu, 26 Oct 2017 02:43:21 GMT
ENV RUBY_DOWNLOAD_SHA256=c2f518eb04b38bdd562ba5611abd2521248a1608fc466368563dd794ddeddd09
# Sat, 04 Nov 2017 02:39:55 GMT
ENV RUBYGEMS_VERSION=2.7.0
# Sat, 04 Nov 2017 02:39:55 GMT
ENV BUNDLER_VERSION=1.16.0
# Sat, 04 Nov 2017 02:42:43 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force
# Sat, 04 Nov 2017 02:42:43 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 04 Nov 2017 02:42:43 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 04 Nov 2017 02:42:43 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Nov 2017 02:42:44 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sat, 04 Nov 2017 02:42:44 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d1d52bc84c959ce2a6002a4aab897e247f2b7a55c1440de500f57e791c7814f3`  
		Last Modified: Mon, 09 Oct 2017 21:52:48 GMT  
		Size: 45.8 MB (45833677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259e90340c1a040510f4401ab1c6a213cfcd826273c165e394fe7113642cbd35`  
		Last Modified: Tue, 10 Oct 2017 03:23:04 GMT  
		Size: 16.2 MB (16212649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e912a3df84503cbab193a207a5373ba7f24e9196bf2e5a4cfd745de7f6075768`  
		Last Modified: Tue, 10 Oct 2017 03:22:59 GMT  
		Size: 206.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54534a4ee2d230fc8394a7fcc8e7a6a5767dae89a7e710921979722922b73b6e`  
		Last Modified: Sat, 04 Nov 2017 03:35:25 GMT  
		Size: 25.2 MB (25161184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a11a9e0098e8b18df1daa39c6e56f27b33f07fa4f64bcc1332b0e934ccc081`  
		Last Modified: Sat, 04 Nov 2017 03:35:15 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:rc-slim` - linux; ppc64le

```console
$ docker pull ruby@sha256:edba05aac48603faae3785e7664eccbe49c0bf7dada436f85848359e59c046e4
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83342027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c2ae6c8f2949a82ed7016527840a3aacbc9a4c4fc875f6c192a4ff927df628b`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 09 Oct 2017 21:45:33 GMT
ADD file:5217c22b771467c9c3563f1e5b1bbd92eff26c36f0dafc6cfed4ba0664f12a45 in / 
# Mon, 09 Oct 2017 21:45:35 GMT
CMD ["bash"]
# Tue, 10 Oct 2017 05:36:19 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 10 Oct 2017 05:36:25 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 26 Oct 2017 00:20:16 GMT
ENV RUBY_MAJOR=2.5-rc
# Thu, 26 Oct 2017 00:20:17 GMT
ENV RUBY_VERSION=2.5.0-preview1
# Thu, 26 Oct 2017 00:20:19 GMT
ENV RUBY_DOWNLOAD_SHA256=c2f518eb04b38bdd562ba5611abd2521248a1608fc466368563dd794ddeddd09
# Sat, 04 Nov 2017 00:20:25 GMT
ENV RUBYGEMS_VERSION=2.7.0
# Sat, 04 Nov 2017 00:20:26 GMT
ENV BUNDLER_VERSION=1.16.0
# Sat, 04 Nov 2017 00:27:01 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force
# Sat, 04 Nov 2017 00:27:02 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 04 Nov 2017 00:27:04 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 04 Nov 2017 00:27:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Nov 2017 00:27:08 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sat, 04 Nov 2017 00:27:09 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:f2df583ad5343147c4ed6ea52882355b70e206e1a801cbb0fe3b6fc6c7b0189a`  
		Last Modified: Mon, 09 Oct 2017 21:52:17 GMT  
		Size: 45.4 MB (45378365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6182431fbc15ee9373459d33bed4e9575bf312d7e1391eeb35d2d4a222d76ab6`  
		Last Modified: Tue, 10 Oct 2017 06:48:33 GMT  
		Size: 12.2 MB (12166035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3140d2a860b9451f510be289090b5ddab2c4ab63a919d3af698534b997d9574f`  
		Last Modified: Tue, 10 Oct 2017 06:48:28 GMT  
		Size: 206.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8cafde6af91f42f547d285e52a8c86d575d097eb0070a2ccee7a4ba899ef050`  
		Last Modified: Sat, 04 Nov 2017 01:33:55 GMT  
		Size: 25.8 MB (25797225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35394c472814079506169b4d992d10276f8972654744f04a9bbe4f106ddcf014`  
		Last Modified: Sat, 04 Nov 2017 01:33:50 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:rc-slim` - linux; s390x

```console
$ docker pull ruby@sha256:8692bc4e78aacf774e3d316fb35131ffd26da9a4af1ed056630e3069b90d9287
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84087081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a5e84c12544d26b5dcf64d7b268023f0c07360c265ceb47eb697fe2a7a6311`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 09 Oct 2017 21:44:19 GMT
ADD file:11704b7d478d6b95a0cfeb557a4a4a03c02fde3849dd3e01da2d1228c6b815f0 in / 
# Mon, 09 Oct 2017 21:44:19 GMT
CMD ["bash"]
# Mon, 09 Oct 2017 23:53:02 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Mon, 09 Oct 2017 23:53:03 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 26 Oct 2017 08:32:00 GMT
ENV RUBY_MAJOR=2.5-rc
# Thu, 26 Oct 2017 08:32:00 GMT
ENV RUBY_VERSION=2.5.0-preview1
# Thu, 26 Oct 2017 08:32:01 GMT
ENV RUBY_DOWNLOAD_SHA256=c2f518eb04b38bdd562ba5611abd2521248a1608fc466368563dd794ddeddd09
# Sat, 04 Nov 2017 08:32:36 GMT
ENV RUBYGEMS_VERSION=2.7.0
# Sat, 04 Nov 2017 08:32:36 GMT
ENV BUNDLER_VERSION=1.16.0
# Sat, 04 Nov 2017 08:34:45 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force
# Sat, 04 Nov 2017 08:34:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 04 Nov 2017 08:34:46 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 04 Nov 2017 08:34:46 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Nov 2017 08:34:47 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sat, 04 Nov 2017 08:34:47 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:c6630da1278315ced68910beef5ac605807b880918d11d0c02c4d3eac7307008`  
		Last Modified: Mon, 09 Oct 2017 21:48:41 GMT  
		Size: 45.0 MB (44972760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8dc9fb89857e80a11a46c0b89653b2fbca9ae06c5781d24e55f93dc65bfe674`  
		Last Modified: Tue, 10 Oct 2017 00:15:39 GMT  
		Size: 13.2 MB (13174350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a4995550c864edc239e5eae3c7fab90f5639e3332c298c3fd64b303e0cc1a4d`  
		Last Modified: Tue, 10 Oct 2017 00:15:34 GMT  
		Size: 206.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40511624eaabc64ddd6c7d191fb434d34a208584eb1c23dbcf8e0083d88710f3`  
		Last Modified: Sat, 04 Nov 2017 09:04:38 GMT  
		Size: 25.9 MB (25939601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e507fc6a41b58b8676761b143c5a12657c52041061d1b3317874ffe10c9e7b8`  
		Last Modified: Sat, 04 Nov 2017 09:04:34 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
