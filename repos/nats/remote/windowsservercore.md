## `nats:windowsservercore`

```console
$ docker pull nats@sha256:05e04d8f9a90a147a093410bd87e1c2bf8afc64d4e1e9246b2cd7c9a12d5fc9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.1770; amd64

### `nats:windowsservercore` - windows version 10.0.14393.1770; amd64

```console
$ docker pull nats@sha256:41a8fdb9df51979f5f9fb450066804470135ef02318d9ff9f3bd2c08e1e5e24b
```

-	Docker Version: 17.06.1-ee-2
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 GB (5352997422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5a1c8f805cfe678520bc2c381983075624ed56c29f1d8922b95261c3180f087`
-	Entrypoint: `["gnatsd"]`
-	Default Command: `["-c","gnatsd.conf"]`

```dockerfile
# Tue, 13 Dec 2016 10:53:31 GMT
RUN Apply image 10.0.14393.0
# Mon, 09 Oct 2017 19:23:50 GMT
RUN Install update 10.0.14393.1770
# Wed, 01 Nov 2017 18:43:12 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 01 Nov 2017 18:43:13 GMT
RUN cmd /S /C #(nop) WORKDIR C:\gnatsd
# Wed, 01 Nov 2017 18:43:15 GMT
RUN cmd /S /C #(nop) COPY file:61c1931f3ccb93e5489015f8e20111fb3b675785d0003458700c148a3daff2df in gnatsd.exe 
# Wed, 01 Nov 2017 18:43:16 GMT
RUN cmd /S /C #(nop) COPY file:8fad70d15db71db30b9945fba2b3d29035a631ee4fe410e797aef6981c2a1879 in gnatsd.conf 
# Wed, 01 Nov 2017 18:43:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222/tcp 6222/tcp 8222/tcp
# Wed, 01 Nov 2017 18:43:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["gnatsd"]
# Wed, 01 Nov 2017 18:43:18 GMT
RUN cmd /S /C #(nop)  CMD ["-c" "gnatsd.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 13 Dec 2016 10:53:31 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8df8e568af76c1c311a1251f6f7402e2a09d14629840c97091beb9ba55419464`  
		Last Modified: Mon, 09 Oct 2017 19:23:50 GMT  
		Size: 1.3 GB (1280521235 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:560588cec88cfe346ccddcff7e035ffffef9246a74e152c048512977e6bfe3b7`  
		Last Modified: Wed, 01 Nov 2017 18:43:57 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5480238d355c01fa7602eff8564de0552f6aef5546c35e375e89d88b63f78fe1`  
		Last Modified: Wed, 01 Nov 2017 18:43:54 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05028ce2a3aa1fafda217211e28877c44b45046f46c599425c5634af11abafdf`  
		Last Modified: Wed, 01 Nov 2017 18:43:53 GMT  
		Size: 2.5 MB (2482285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f9c6124b2d8702778890a954d9c9541fda40cc3d52f2fc19b217f3e7d52a6e`  
		Last Modified: Wed, 01 Nov 2017 18:43:51 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a16d8982d43fabeffa9435fc1de1feeb708a4555b48a7c9c99d71fda0a6c41`  
		Last Modified: Wed, 01 Nov 2017 18:43:51 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff6880bdc20297fd9c73ac5e502cfb905b862e2f5339657a3e6ec02f48da150`  
		Last Modified: Wed, 01 Nov 2017 18:43:51 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f35fc76bcc6194c2a2df48e86172d592c27da5994ecbc6c275195369487d3c6`  
		Last Modified: Wed, 01 Nov 2017 18:43:52 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
