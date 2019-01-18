# My Blog
http://blog.auska.win

## Usage

```
docker create --name=baidupcs \
-v <path to downloads>:/root/Downloads \
-v <path to config>:/defaults \
-e PGID=<gid> -e PUID=<uid> \
-e TZ=<timezone> \
-e PORT=1999 \  #(port should be greater than 1024)
-p 1999:1999 \  
auska/docker-baidupcs
```


### User / Group Identifiers

Sometimes when using data volumes (`-v` flags) permissions issues can arise between the host OS and the container. We avoid this issue by allowing you to specify the user `PUID` and group `PGID`. Ensure the data volume directory on the host is owned by the same user you specify and it will "just work" ™.

In this instance `PUID=1001` and `PGID=1001`. To find yours use `id user` as below:

```
  $ id <dockeruser>
    uid=1001(dockeruser) gid=1001(dockergroup) groups=1001(dockergroup)
```

## Versions

+ **3.5.7:** Rebase to alpine linux 3.8.
+ **3.5.8:** Update 3.5.8.
+ **3.5.9:** Update 3.5.9.
+ **3.6.1:** Update 3.6.1.
+ **3.6.2:** Update 3.6.2.

## Refferences
https://github.com/liuzhuoling2011/baidupcs-web

https://github.com/iikira/BaiduPCS-Go
