## `ubuntu:trusty`

```console
$ docker pull ubuntu@sha256:f6eed4def93a3b54da920737f0abf1a8cae2e480bb368280c898265fcaf910a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `ubuntu:trusty` - linux; amd64

```console
$ docker pull ubuntu@sha256:70caab365fb71f2d68b09caed135dce234cf36d2d32f39243d969386d1468890
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67188934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aa18c7568fc27f60836c67a0f74947b64da3555978b8437a0be8a23b988d9a2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 04 Nov 2017 09:45:18 GMT
ADD file:8f997234193c2f587ac17bb4a8db2657103d2924813edb281eec7ba9883a2806 in / 
# Sat, 04 Nov 2017 09:45:19 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Sat, 04 Nov 2017 09:45:20 GMT
RUN rm -rf /var/lib/apt/lists/*
# Sat, 04 Nov 2017 09:45:20 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Sat, 04 Nov 2017 09:45:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Sat, 04 Nov 2017 09:45:21 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bae382666908fd87a3a3646d7eb7176fa42226027d3256cac38ee0b79bdb0491`  
		Last Modified: Wed, 13 Sep 2017 22:04:42 GMT  
		Size: 67.1 MB (67114903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ddd5e846a849fff877e4d61dc1002ca5d51de8521cced522e9503312b4c4e7`  
		Last Modified: Sat, 04 Nov 2017 09:46:17 GMT  
		Size: 72.7 KB (72653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d12f864ab9d4cfe6475fc7ba508327c26d3d624344d6584a1fd860c3f0fefa`  
		Last Modified: Sat, 04 Nov 2017 09:46:18 GMT  
		Size: 364.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57ea72e31769e58f0c36db12d25683eba8fa14aaab0518729f28b3766b01112`  
		Last Modified: Sat, 04 Nov 2017 09:46:19 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783a14252520746e3f7fee937b5f14ac1a84ef248ea0b1343d8b58b96df3fa9f`  
		Last Modified: Sat, 04 Nov 2017 09:46:17 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:trusty` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:0a92fed07024ea15648f92e3209a76276194087de3d15a17a7eedfcc070d1c84
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61533399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4859790a66d87a06b3a99b9e65c686f6eb69de1d8ed98833163de1f88f76f60d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 27 Sep 2017 04:14:46 GMT
ADD file:9269eeb4eb9940532bc07ce41e27a91f440fe57993b35cb2ccbabf18e6e08937 in / 
# Wed, 27 Sep 2017 04:14:47 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 27 Sep 2017 04:14:48 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 27 Sep 2017 04:14:50 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Wed, 27 Sep 2017 04:14:50 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 27 Sep 2017 04:14:51 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:187f4a01d8b8e7f7d189098d4bcec67814384806cd4c813fc7e4b377f145045a`  
		Last Modified: Wed, 27 Sep 2017 04:16:17 GMT  
		Size: 61.5 MB (61455216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:682e73a2927e06cb0dce96383ca5174e23b9f24ca554c8cfcec1e47c3941bfad`  
		Last Modified: Wed, 27 Sep 2017 04:15:56 GMT  
		Size: 76.8 KB (76773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b564854d4c33a8370ba24496f183cbcd732c0da282e49512324c1816cd105dad`  
		Last Modified: Wed, 27 Sep 2017 04:15:56 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b48a5540d3c6fc9c465039823d1d0a07c4e038eba6875ca638b4e1d69133dbc4`  
		Last Modified: Wed, 27 Sep 2017 04:15:56 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561af84b7f63d18054cfc85b75035f9a6bf64ddcba38af1bc3777416c9c754cf`  
		Last Modified: Wed, 27 Sep 2017 04:15:56 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:trusty` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:61de5c00451887fb0f98af9a1c989dd983e7c65f5b6c884d85ca8a5d49cdfc53
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63229037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbb6f732d326019e135cfedabcef425153a53081758db52af9cebbe4ecd65ef7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Sep 2017 23:27:01 GMT
ADD file:7ea2c29a53add06a8c5849caffdfcc5171d9cc0de439687b73167ee8c8c6a995 in / 
# Wed, 13 Sep 2017 23:27:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 13 Sep 2017 23:27:04 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 13 Sep 2017 23:27:09 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Wed, 13 Sep 2017 23:27:10 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 13 Sep 2017 23:27:11 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:211fe73d577b3db63c2f5ce11a7f9403edecb4977eee8574e2a53fdf02fd42d3`  
		Last Modified: Wed, 13 Sep 2017 23:29:18 GMT  
		Size: 63.2 MB (63168561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dcade08d581afdb20d6dbca47eb05d2598554917f214718e928b70a48b54f39`  
		Last Modified: Wed, 13 Sep 2017 23:28:54 GMT  
		Size: 59.1 KB (59097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:712265ae9a89af70df71abdfff24731189ca5339030894a8656a46dea59c7206`  
		Last Modified: Wed, 13 Sep 2017 23:28:54 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a26e33b782f6f9e0f19992a733d18b44cfcf53d86feea2ad3f55dfd7d652bba`  
		Last Modified: Wed, 13 Sep 2017 23:28:54 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d05d097f34378dbf6ca969f9256f553f25b24a3b11f6ee48651c6405a4e81abb`  
		Last Modified: Wed, 13 Sep 2017 23:28:53 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:trusty` - linux; 386

```console
$ docker pull ubuntu@sha256:1450570906d2ee1a87a61c3524d7275a33e8b13178ac683ca17eb1af1a13c527
```

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64898863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07a65d981ede1fe04f76aae7decaaf10eb793442a5327674f8fed1a518f27043`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Sep 2017 23:26:25 GMT
ADD file:5ea4259718526648d5d282e8d9d1c2584e856b39c0f4b8594de9aa9f9985218b in / 
# Wed, 13 Sep 2017 23:26:25 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 13 Sep 2017 23:26:26 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 13 Sep 2017 23:26:27 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Wed, 13 Sep 2017 23:26:27 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 13 Sep 2017 23:26:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f783391c63c08ef35d2d6263d1009541806f2358ba987368c7abf8729cf5d577`  
		Last Modified: Wed, 06 Sep 2017 09:36:00 GMT  
		Size: 64.8 MB (64832640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a47d2c69876192779226a84caa6f71f9c15cf4151b85c06c3f6289423c5259`  
		Last Modified: Wed, 13 Sep 2017 23:27:26 GMT  
		Size: 64.9 KB (64851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00cd5494581ef496db53eae6ef74ee4589a5d2f2d53faede541254b65eee6a0`  
		Last Modified: Wed, 13 Sep 2017 23:27:25 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f705fb93233929d4f280117ab56b4fa4666a06a975de96a8279bd985bd3f1e`  
		Last Modified: Wed, 13 Sep 2017 23:27:26 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd11b43477b7c801f64151e30c383653655af3332787fed6204add3ab092753`  
		Last Modified: Wed, 13 Sep 2017 23:27:25 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:trusty` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:cc5836604afdf422e82cb383611a30a00cef2b507da0187e715aeaa35c0b3248
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69765624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d24e7893481921724c46a7e622bbebf49ec40cf0c68fcb5828937fa23494d8ad`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Sep 2017 23:27:59 GMT
ADD file:ecdc3f73d8b16947cc3eee78b4e1f5a5431029720cabb5a589e91f72d560567b in / 
# Wed, 13 Sep 2017 23:28:06 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 13 Sep 2017 23:28:10 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 13 Sep 2017 23:28:14 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Wed, 13 Sep 2017 23:28:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 13 Sep 2017 23:28:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:06cef575e03acca24a1e636f8d2ed694a09a1296706cce34cdab56ff4e6cdeec`  
		Last Modified: Wed, 13 Sep 2017 23:31:02 GMT  
		Size: 69.7 MB (69700798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:037f9273c8ba936000db3a181323c6fd5591e70339a659470b90d4b0c1c9162d`  
		Last Modified: Wed, 13 Sep 2017 23:30:43 GMT  
		Size: 63.4 KB (63417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f10fea324280b832d0e4ff046f0269c66baa2eca54efc73917c6510c8be844`  
		Last Modified: Wed, 13 Sep 2017 23:30:43 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f301276d41ce9d2379e7b962e2ee5a3040e0f14eef21e66136125a3100fae46c`  
		Last Modified: Wed, 13 Sep 2017 23:30:43 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5a488e2380e445d07718060469f8afc534131480e6b012179e2e5f5884e28c`  
		Last Modified: Wed, 13 Sep 2017 23:30:43 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
