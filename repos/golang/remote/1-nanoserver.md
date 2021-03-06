## `golang:1-nanoserver`

```console
$ docker pull golang@sha256:053110f25114c92c7efee12ad21edd2fb9ba5bf496dab538b7664545a505d17e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.1770; amd64

### `golang:1-nanoserver` - windows version 10.0.14393.1770; amd64

```console
$ docker pull golang@sha256:f24f4a9d8ff9be941ec8c1dd06fd9b8a09c3893c76aae2adf0a57b2c77957a60
```

-	Docker Version: 17.06.1-ee-2
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **501.7 MB (501675791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:823f99ac7b5bf4a1fcfa68fbdc8f12c8e4e371a8c460aa623de45bbfdea585c6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Tue, 13 Dec 2016 10:47:17 GMT
RUN Apply image 10.0.14393.0
# Mon, 09 Oct 2017 19:23:15 GMT
RUN Install update 10.0.14393.1770
# Wed, 01 Nov 2017 19:10:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 01 Nov 2017 20:33:13 GMT
ENV GOPATH=C:\gopath
# Wed, 01 Nov 2017 20:33:37 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath;
# Wed, 01 Nov 2017 20:33:38 GMT
ENV GOLANG_VERSION=1.9.2
# Wed, 01 Nov 2017 20:37:39 GMT
RUN $url = ('https://golang.org/dl/go{0}.windows-amd64.zip' -f $env:GOLANG_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '682ec3626a9c45b657c2456e35cadad119057408d37f334c6c24d88389c2164c'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Complete.';
# Wed, 01 Nov 2017 20:37:40 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:bce2fbc256ea437a87dadac2f69aabd25bed4f56255549090056c1131fad0277`  
		Last Modified: Tue, 13 Dec 2016 10:47:17 GMT  
		Size: 252.7 MB (252691002 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b0b5e40cb939a7befa4e01212d6f65f30022bbd04b5f15985b45ce9cfd3fcabc`  
		Last Modified: Mon, 09 Oct 2017 19:23:15 GMT  
		Size: 141.8 MB (141758132 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a9382483e5965aea803961361c0487953f0cd98ba1d8dbc82a8fe13ea156788d`  
		Last Modified: Wed, 01 Nov 2017 19:18:19 GMT  
		Size: 925.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c8d3d75a1aca31e0860ff222016aefb0368d286af1c27d91a892d7e210f10a6`  
		Last Modified: Wed, 01 Nov 2017 20:47:32 GMT  
		Size: 923.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:740d34d6440436d981b007231acf90c0f7ac431231cbddb30b5eb34143318ce0`  
		Last Modified: Wed, 01 Nov 2017 20:47:32 GMT  
		Size: 904.4 KB (904387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6f8ba1442115231d4e129a64445acde1124719c6321c1f6b816de3d2a2edc0`  
		Last Modified: Wed, 01 Nov 2017 20:47:32 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9658d90421ffdecff4a188a51c01acbd2a28add83f0429f779bdb92a14327a54`  
		Last Modified: Wed, 01 Nov 2017 20:47:54 GMT  
		Size: 106.3 MB (106318316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1282ba5ba22de6d28c839a822bffd98e83d5e7ee9268fc4233679b81fa5150e`  
		Last Modified: Wed, 01 Nov 2017 20:47:32 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
