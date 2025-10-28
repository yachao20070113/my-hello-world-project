yachao20070113@localhost:~/my-hello-world-project$ docker images
REPOSITORY    TAG       IMAGE ID       CREATED        SIZE
test/ubuntu   v1        34c7b9491f69   3 days ago     4.81kB
python        3         78ad0471881f   2 weeks ago    1.61GB
ubuntu        latest    66460d557b25   3 weeks ago    117MB
hello-world   latest    6dc565aa6309   2 months ago   20.3kB
ubuntu        20.04     8feb4d8ca535   6 months ago   109MB
ubuntu        15.10     20122b67efbb   55 years ago   4.54kB
yachao20070113@localhost:~/my-hello-world-project$ docker run -t -i ubuntu:20.04 
/bin/bash 
root@e1b689deefa4:/# ^C
root@e1b689deefa4:/# exit
exit
yachao20070113@localhost:~/my-hello-world-project$ docker pull ubuntu:13.10
Error response from daemon: not implemented: media type "application/vnd.docker.distribution.manifest.v1+prettyjws" is no longer supported since containerd v2.1, please rebuild the image as "application/vnd.docker.distribution.manifest.v2+json" or "application/vnd.oci.image.manifest.v1+json"
yachao20070113@localhost:~/my-hello-world-project$ ^C
yachao20070113@localhost:~/my-hello-world-project$ docker search httpd
NAME                     DESCRIPTION                                     STARS     OFFICIAL
httpd                    The Apache HTTP Server Project                  4906      [OK]
manageiq/httpd           Container with httpd, built on CentOS for Ma…   1         
paketobuildpacks/httpd                                                   0         
vulhub/httpd                                                             0         
openeuler/httpd                                                          0         
dockerpinata/httpd                                                       1         
centos/httpd                                                             36        
manasip/httpd                                                            0         
e2eteam/httpd                                                            0         
amd64/httpd              The Apache HTTP Server Project                  1         
futdryt/httpd                                                            0         
arm64v8/httpd            The Apache HTTP Server Project                  11        
signiant/httpd           httpd (apache2) base container with a custom…   0         
ppc64le/httpd            The Apache HTTP Server Project                  0         
9af925e7043/httpd                                                        0         
arm32v7/httpd            The Apache HTTP Server Project                  11        
s390x/httpd              The Apache HTTP Server Project                  1         
i386/httpd               The Apache HTTP Server Project                  1         
tugboatqa/httpd          The Apache HTTP Server Project                  0         
aerzas/httpd             HTTPD docker container image that requires n…   0         
publici/httpd            httpd:latest                                    1         
inventis/httpd           apache container with support for https only    0         
buzzardev/httpd          Based on the official httpd image               0         
armhf/httpd              The Apache HTTP Server Project                  8         
appertly/httpd           Customized Apache HTTPD that uses a PHP-FPM …   0         
yachao20070113@localhost:~/my-hello-world-project$ docker pull httpd #下载镜像
Using default tag: latest
latest: Pulling from library/httpd
38513bd72563: Pulling fs layer 
72ba0317f875: Pull complete 
4f4fb700ef54: Pull complete 
a6c97c1311d6: Pull complete 
37be031b3615: Pull complete 
359a248d4bde: Pull complete 
Digest: sha256:d3b88ca0822f91e2dec6eb58a2ac7cfade27880926467fc63dcdbc857010b083
Status: Downloaded newer image for httpd:latest
docker.io/library/httpd:latest
yachao20070113@localhost:~/my-hello-world-project$ docker run httpd #运行镜像
yachao20070113@localhost:~/my-hello-world-project$ docker images 
REPOSITORY    TAG       IMAGE ID       CREATED        SIZE
test/ubuntu   v1        34c7b9491f69   3 days ago     4.81kB
python        3         78ad0471881f   2 weeks ago    1.61GB
ubuntu        latest    66460d557b25   3 weeks ago    117MB
httpd         latest    d3b88ca0822f   2 months ago   175MB
ubuntu        20.04     8feb4d8ca535   6 months ago   109MB
ubuntu        15.10     20122b67efbb   55 years ago   4.54kB
yachao20070113@localhost:~/my-hello-world-project$ docker tag 34c7b9491f69 test/ubuntu:dev
yachao20070113@localhost:~/my-hello-world-project$ docker images
REPOSITORY    TAG       IMAGE ID       CREATED        SIZE
test/ubuntu   dev       34c7b9491f69   3 days ago     4.81kB
test/ubuntu   v1        34c7b9491f69   3 days ago     4.81kB
python        3         78ad0471881f   2 weeks ago    1.61GB
ubuntu        latest    66460d557b25   3 weeks ago    117MB
httpd         latest    d3b88ca0822f   2 months ago   175MB
ubuntu        20.04     8feb4d8ca535   6 months ago   109MB
ubuntu        15.10     20122b67efbb   55 years ago   4.54kB