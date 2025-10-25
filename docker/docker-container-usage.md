yachao20070113@localhost:~/my-hello-world-project$ docker
Usage:  docker [OPTIONS] COMMAND

A self-sufficient runtime for containers

Common Commands:
  run         Create and run a new container from an image
  exec        Execute a command in a running container
  ps          List containers
  build       Build an image from a Dockerfile
  bake        Build from a file
  pull        Download an image from a registry
  push        Upload an image to a registry
  images      List images
  login       Authenticate to a registry
  logout      Log out from a registry
  search      Search Docker Hub for images
  version     Show the Docker version information
  info        Display system-wide information

Management Commands:
  ai*         Docker AI Agent - Ask Gordon
  builder     Manage builds
  buildx*     Docker Buildx
  cloud*      Docker Cloud
  compose*    Docker Compose
  container   Manage containers
  context     Manage contexts
  debug*      Get a shell into any image or container
  desktop*    Docker Desktop commands
  extension*  Manages Docker extensions
  image       Manage images
  init*       Creates Docker-related starter files for your project
  manifest    Manage Docker image manifests and manifest lists
  mcp*        Docker MCP Plugin
  model*      Docker Model Runner
  network     Manage networks
  plugin      Manage plugins
  sbom*       View the packaged-based Software Bill Of Materials (SBOM) for an image
  scout*      Docker Scout
  system      Manage Docker
  trust       Manage trust on Docker images
  volume      Manage volumes

Swarm Commands:
  swarm       Manage Swarm

Commands:
  attach      Attach local standard input, output, and error streams to a running container
  commit      Create a new image from a container's changes
  cp          Copy files/folders between a container and the local filesystem
  create      Create a new container
  diff        Inspect changes to files or directories on a container's filesystem
  events      Get real time events from the server
  export      Export a container's filesystem as a tar archive
  history     Show the history of an image
  import      Import the contents from a tarball to create a filesystem image
  inspect     Return low-level information on Docker objects
  kill        Kill one or more running containers
  load        Load an image from a tar archive or STDIN
  logs        Fetch the logs of a container
  pause       Pause all processes within one or more containers
  port        List port mappings or a specific mapping for the container
  rename      Rename a container
  restart     Restart one or more containers
  rm          Remove one or more containers
  rmi         Remove one or more images
  save        Save one or more images to a tar archive (streamed to STDOUT by default)
  start       Start one or more stopped containers
  stats       Display a live stream of container(s) resource usage statistics
  stop        Stop one or more running containers
  tag         Create a tag TARGET_IMAGE that refers to SOURCE_IMAGE
  top         Display the running processes of a container
  unpause     Unpause all processes within one or more containers
  update      Update configuration of one or more containers
  wait        Block until one or more containers stop, then print their exit codes

Global Options:
      --config string      Location of client config files (default
                           "/home/yachao20070113/.docker")
  -c, --context string     Name of the context to use to connect to the
                           daemon (overrides DOCKER_HOST env var and
                           default context set with "docker context use")
  -D, --debug              Enable debug mode
  -H, --host string        Daemon socket to connect to
  -l, --log-level string   Set the logging level ("debug", "info",
                           "warn", "error", "fatal") (default "info")
      --tls                Use TLS; implied by --tlsverify
      --tlscacert string   Trust certs signed only by this CA (default
                           "/home/yachao20070113/.docker/ca.pem")
      --tlscert string     Path to TLS certificate file (default
                           "/home/yachao20070113/.docker/cert.pem")
      --tlskey string      Path to TLS key file (default
                           "/home/yachao20070113/.docker/key.pem")
      --tlsverify          Use TLS and verify the remote
  -v, --version            Print version information and quit

Run 'docker COMMAND --help' for more information on a command.

For more help on how to use Docker, head to https://docs.docker.com/go/guides/
yachao20070113@localhost:~/my-hello-world-project$  docker stats --help
Usage:  docker stats [OPTIONS] [CONTAINER...]

Display a live stream of container(s) resource usage statistics

Aliases:
  docker container stats, docker stats

Options:
  -a, --all             Show all containers (default shows just running)
      --format string   Format output using a custom template:
                        'table':            Print output in table format
                        with column headers (default)
                        'table TEMPLATE':   Print output in table format
                        using the given Go template
                        'json':             Print in JSON format
                        'TEMPLATE':         Print output using the given
                        Go template.
                        Refer to https://docs.docker.com/go/formatting/
                        for more information about formatting output with
                        templates
      --no-stream       Disable streaming stats and only pull the first result
      --no-trunc        Do not truncate output
yachao20070113@localhost:~/my-hello-world-project$ docker pull ubuntu
Using default tag: latest
latest: Pulling from library/ubuntu
Digest: sha256:66460d557b25769b102175144d538d88219c077c678a49af4afca6fbfc1b5252
Status: Image is up to date for ubuntu:latest
docker.io/library/ubuntu:latest
yachao20070113@localhost:~/my-hello-world-project$ docker run -it ubuntu /bin/bash
root@bd46f6537726:/# exit
exit
yachao20070113@localhost:~/my-hello-world-project$  docker ps -a
CONTAINER ID   IMAGE          COMMAND                  CREATED          STATUS                      PORTS     NAMES
bd46f6537726   ubuntu         "/bin/bash"              29 seconds ago   Exited (0) 17 seconds ago             youthful_yalow
778eee43b980   ubuntu         "/bin/bash"              13 minutes ago   Up 11 minutes                         ubuntu-test
97bc5b3a5db8   ubuntu         "/bin/bash"              17 minutes ago   Up 14 minutes                         beautiful_bartik
1eccbbf0bd82   ubuntu:20.04   "/bin/echo 'Hello wo…"   30 hours ago     Exited (0) 30 hours ago               youthful_vaughan
78a9b42ef3d7   ubuntu:20.04   "/bin/sh -c 'while t…"   3 days ago       Exited (137) 3 days ago               nervous_curie
d5ac35c4e6ae   ubuntu:20.04   "/bin/bash"              3 days ago       Exited (0) 3 days ago                 jolly_yonath
ff696ed2f149   ubuntu:20.04   "/bin/echo 'Hello wo…"   3 days ago       Exited (0) 3 days ago                 sad_keller
8110b24fdd0e   ubuntu:20.04   "/bin/bash"              3 days ago       Exited (129) 3 days ago               nifty_jang
59e16c7c33da   ubuntu:20.04   "/bin/sh -c 'while t…"   3 days ago       Exited (255) 30 hours ago             wonderful_wu
83eb43cec122   ubuntu:20.04   "/bin/sh -c 'while t…"   3 days ago       Exited (255) 30 hours ago             relaxed_archimedes
e5bc55d8808f   ubuntu:20.04   "/bin/bash"              3 days ago       Exited (0) 3 days ago                 infallible_khayyam
0addceb0efb1   ubuntu:20.04   "/bin/echo 'Hello wo…"   3 days ago       Exited (0) 3 days ago                 adoring_goldstine
245819f6cb08   ubuntu:20.04   "/bin/echo 'Hello wo…"   3 days ago       Exited (0) 3 days ago                 affectionate_gould
8516fa97e211   ubuntu:20.04   "/bin/bash"              5 days ago       Exited (255) 3 days ago               priceless_wing
cd41288536db   hello-world    "/hello"                 5 days ago       Exited (0) 5 days ago                 laughing_wilson
yachao20070113@localhost:~/my-hello-world-project$ docker start^C
yachao20070113@localhost:~/my-hello-world-project$ docker start bd46f6537726
bd46f6537726
yachao20070113@localhost:~/my-hello-world-project$ docker run -itd --name ubuntu-test ubuntu /bin/bash
docker: Error response from daemon: Conflict. The container name "/ubuntu-test" is already in use by container "778eee43b9803f778a073a30b8536c5d493c05cb01c369b0697475bce9c2c976". You have to remove (or rename) that container to be able to reuse that name.

Run 'docker run --help' for more information
yachao20070113@localhost:~/my-hello-world-project$ docker run -itd --name ubuntu-test ubuntu /bin/bash
docker: Error response from daemon: Conflict. The container name "/ubuntu-test" is already in use by container "778eee43b9803f778a073a30b8536c5d493c05cb01c369b0697475bce9c2c976". You have to remove (or rename) that container to be able to reuse that name.

Run 'docker run --help' for more information
yachao20070113@localhost:~/my-hello-world-project$ docker export bd46f6537726 > 
ubuntu.tar
yachao20070113@localhost:~/my-hello-world-project$ cat docker/ubuntu.tar | docker import - test/ubuntu:v1
cat: docker/ubuntu.tar: No such file or directory
sha256:34c7b9491f69d5a95ddfc73c70624cce49f075ff47ff93e3ca4fa47d6c5681c8
yachao20070113@localhost:~/my-hello-world-project$ docker rm -f^C
yachao20070113@localhost:~/my-hello-world-project$ docker rm -f bd46f6537726
bd46f6537726
yachao20070113@localhost:~/my-hello-world-project$ docker container prune
WARNING! This will remove all stopped containers.
Are you sure you want to continue? [y/N] y
Deleted Containers:
1eccbbf0bd82f524e0b8581d0edad4cc1eb3a13000d8147530795e5594b55b9e
78a9b42ef3d7aadcb519b52663b1f8fcc19b2627b506ae7935b39e4f4bdfe40e
d5ac35c4e6ae8d2bc8eb48a85fa2c60a0bfa1e65f6f88d8328ca5c606d5afba3
ff696ed2f149267fc596e427e4f15bbcb8cdfb62fbd658076c8cd218a889f6e0
8110b24fdd0efa2a5cc8f058d0583d9636459e958f0c615de6735f096f7c37a8
59e16c7c33da37a265bec419124e8cfec4d2a6a2987ece732dcdd4e63c9ace34
83eb43cec1220361434e0be023b2442b72cb62116df431750556ec1c99f40e22
e5bc55d8808fcb177849de1a888be6a41fea2d3e08bb46b9e7e8acb18147ea44
0addceb0efb1c1ffa9acadad640756741ab6fc374df23613463b17d769aef4ab
245819f6cb08a446dac5b96e37236f8f4d0df52d0a9c8f18f62fb8d9acc909ad
8516fa97e2117d82b181aa62a0bc77f06435e472a8727c7043e0604487af5dd7
cd41288536db4920495c8cd9678fd4ad6d925c60dc0ede4b18fd08998be8a0e1

Total reclaimed space: 73.73kB
yachao20070113@localhost:~/my-hello-world-project$ docker pull training/webapp
Using default tag: latest
Error response from daemon: not implemented: media type "application/vnd.docker.distribution.manifest.v1+prettyjws" is no longer supported since containerd v2.1, please rebuild the image as "application/vnd.docker.distribution.manifest.v2+json" or "application/vnd.oci.image.manifest.v1+json"
yachao20070113@localhost:~/my-hello-world-project$ docker run -d -P training/webapp python app.py
Unable to find image 'training/webapp:latest' locally
docker: Error response from daemon: not implemented: media type "application/vnd.docker.distribution.manifest.v1+prettyjws" is no longer supported since containerd v2.1, please rebuild the image as "application/vnd.docker.distribution.manifest.v2+json" or "application/vnd.oci.image.manifest.v1+json"

Run 'docker run --help' for more information
yachao20070113@localhost:~/my-hello-world-project$ docker run -it ubuntu /bin/bash
root@ada6e9a575e8:/# exit
exit
yachao20070113@localhost:~/my-hello-world-project$ docker pull training/webapp
Using default tag: latest
Error response from daemon: not implemented: media type "application/vnd.docker.distribution.manifest.v1+prettyjws" is no longer supported since containerd v2.1, please rebuild the image as "application/vnd.docker.distribution.manifest.v2+json" or "application/vnd.oci.image.manifest.v1+json"
yachao20070113@localhost:~/my-hello-world-project$ docker pull ubuntu
Using default tag: latest
Error response from daemon: failed to resolve reference "docker.io/library/ubuntu:latest": failed to authorize: failed to fetch anonymous token: Get "https://auth.docker.io/token?scope=repository%3Alibrary%2Fubuntu%3Apull&service=registry.docker.io": unexpected EOF
yachao20070113@localhost:~/my-hello-world-project$ docker run -d -P training/webapp python app.py
Unable to find image 'training/webapp:latest' locally
docker: Error response from daemon: not implemented: media type "application/vnd.docker.distribution.manifest.v1+prettyjws" is no longer supported since containerd v2.1, please rebuild the image as "application/vnd.docker.distribution.manifest.v2+json" or "application/vnd.oci.image.manifest.v1+json"

Run 'docker run --help' for more information
yachao20070113@localhost:~/my-hello-world-project$ sudo containerd --version
[sudo] password for yachao20070113: 
sudo: containerd: command not found
yachao20070113@localhost:~/my-hello-world-project$                              
docker build -t your-username/webapp:new-tag .
[+] Building 0.1s (1/1) FINISHED                                 docker:default
 => [internal] load build definition from Dockerfile                       0.1s
 => => transferring dockerfile: 2B                                         0.0s
ERROR: failed to build: failed to solve: failed to read dockerfile: open Dockerfile: no such file or directory
yachao20070113@localhost:~/my-hello-world-project$ docker ps
CONTAINER ID   IMAGE     COMMAND       CREATED          STATUS          PORTS     NAMES
778eee43b980   ubuntu    "/bin/bash"   42 minutes ago   Up 39 minutes             ubuntu-test
97bc5b3a5db8   ubuntu    "/bin/bash"   46 minutes ago   Up 43 minutes             beautiful_bartik
yachao20070113@localhost:~/my-hello-world-project$ docker pull ubuntu
Using default tag: latest
latest: Pulling from library/ubuntu
Digest: sha256:66460d557b25769b102175144d538d88219c077c678a49af4afca6fbfc1b5252
Status: Image is up to date for ubuntu:latest
docker.io/library/ubuntu:latest
yachao20070113@localhost:~/my-hello-world-project$ docker run -d -P ubuntu app p
ython app.py
fb823e2691f2587d92b417b21191cfe260577c683288a017e64c6230a50eec90
docker: Error response from daemon: failed to create task for container: failed to create shim task: OCI runtime create failed: runc create failed: unable to start container process: error during container init: exec: "app": executable file not found in $PATH: unknown

Run 'docker run --help' for more information
yachao20070113@localhost:~/my-hello-world-project$ docker run -it --name my_ptthon ubuntu bash
root@f3c678f04cee:/# apt update && apt install -y python3
Get:1 http://security.ubuntu.com/ubuntu noble-security InRelease [126 kB]
Get:2 http://archive.ubuntu.com/ubuntu noble InRelease [256 kB]
Get:3 http://security.ubuntu.com/ubuntu noble-security/universe amd64 Packages [1167 kB]
Get:4 http://archive.ubuntu.com/ubuntu noble-updates InRelease [126 kB]        
Get:5 http://archive.ubuntu.com/ubuntu noble-backports InRelease [126 kB]
Get:6 http://security.ubuntu.com/ubuntu noble-security/main amd64 Packages [1587 kB]
Get:7 http://archive.ubuntu.com/ubuntu noble/multiverse amd64 Packages [331 kB]
Get:8 http://security.ubuntu.com/ubuntu noble-security/restricted amd64 Packages [2624 kB]
Get:9 http://security.ubuntu.com/ubuntu noble-security/multiverse amd64 Packages [33.1 kB]
Get:10 http://archive.ubuntu.com/ubuntu noble/universe amd64 Packages [19.3 MB]
Get:11 http://archive.ubuntu.com/ubuntu noble/main amd64 Packages [1808 kB]    
Get:12 http://archive.ubuntu.com/ubuntu noble/restricted amd64 Packages [117 kB]
Get:13 http://archive.ubuntu.com/ubuntu noble-updates/main amd64 Packages [1952 kB]
Get:14 http://archive.ubuntu.com/ubuntu noble-updates/multiverse amd64 Packages [35.9 kB]
Get:15 http://archive.ubuntu.com/ubuntu noble-updates/restricted amd64 Packages [2754 kB]
Get:16 http://archive.ubuntu.com/ubuntu noble-updates/universe amd64 Packages [1937 kB]
Get:17 http://archive.ubuntu.com/ubuntu noble-backports/universe amd64 Packages [33.9 kB]
Get:18 http://archive.ubuntu.com/ubuntu noble-backports/main amd64 Packages [49.4 kB]
Fetched 34.4 MB in 51s (668 kB/s)                                              
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
2 packages can be upgraded. Run 'apt list --upgradable' to see them.
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following additional packages will be installed:
  ca-certificates libexpat1 libpython3-stdlib libpython3.12-minimal
  libpython3.12-stdlib libreadline8t64 libsqlite3-0 media-types netbase
  openssl python3-minimal python3.12 python3.12-minimal readline-common tzdata
Suggested packages:
  python3-doc python3-tk python3-venv python3.12-venv python3.12-doc binutils
  binfmt-support readline-doc
The following NEW packages will be installed:
  ca-certificates libexpat1 libpython3-stdlib libpython3.12-minimal
  libpython3.12-stdlib libreadline8t64 libsqlite3-0 media-types netbase
  openssl python3 python3-minimal python3.12 python3.12-minimal
  readline-common tzdata
0 upgraded, 16 newly installed, 0 to remove and 2 not upgraded.
Need to get 8426 kB of archives.
After this operation, 30.2 MB of additional disk space will be used.
Get:1 http://archive.ubuntu.com/ubuntu noble-updates/main amd64 libpython3.12-minimal amd64 3.12.3-1ubuntu0.8 [836 kB]
Get:2 http://archive.ubuntu.com/ubuntu noble-updates/main amd64 libexpat1 amd64 2.6.1-2ubuntu0.3 [88.0 kB]
Get:3 http://archive.ubuntu.com/ubuntu noble-updates/main amd64 python3.12-minimal amd64 3.12.3-1ubuntu0.8 [2334 kB]
Get:4 http://archive.ubuntu.com/ubuntu noble-updates/main amd64 python3-minimal amd64 3.12.3-0ubuntu2 [27.4 kB]
Get:5 http://archive.ubuntu.com/ubuntu noble/main amd64 media-types all 10.1.0 [27.5 kB]
Get:6 http://archive.ubuntu.com/ubuntu noble/main amd64 netbase all 6.4 [13.1 kB]
Get:7 http://archive.ubuntu.com/ubuntu noble-updates/main amd64 tzdata all 2025b-0ubuntu0.24.04.1 [276 kB]
Get:8 http://archive.ubuntu.com/ubuntu noble/main amd64 readline-common all 8.2-4build1 [56.5 kB]
Get:9 http://archive.ubuntu.com/ubuntu noble/main amd64 libreadline8t64 amd64 8.2-4build1 [153 kB]
Get:10 http://archive.ubuntu.com/ubuntu noble-updates/main amd64 libsqlite3-0 amd64 3.45.1-1ubuntu2.5 [701 kB]
Get:11 http://archive.ubuntu.com/ubuntu noble-updates/main amd64 libpython3.12-stdlib amd64 3.12.3-1ubuntu0.8 [2068 kB]
Get:12 http://archive.ubuntu.com/ubuntu noble-updates/main amd64 python3.12 amd64 3.12.3-1ubuntu0.8 [651 kB]
Get:13 http://archive.ubuntu.com/ubuntu noble-updates/main amd64 libpython3-stdlib amd64 3.12.3-0ubuntu2 [10.0 kB]
Get:14 http://archive.ubuntu.com/ubuntu noble-updates/main amd64 python3 amd64 3.12.3-0ubuntu2 [23.0 kB]
Get:15 http://archive.ubuntu.com/ubuntu noble-updates/main amd64 openssl amd64 3.0.13-0ubuntu3.6 [1003 kB]
Get:16 http://archive.ubuntu.com/ubuntu noble/main amd64 ca-certificates all 20240203 [159 kB]
Fetched 8426 kB in 35s (244 kB/s)                                              
debconf: delaying package configuration, since apt-utils is not installed
Selecting previously unselected package libpython3.12-minimal:amd64.
(Reading database ... 4381 files and directories currently installed.)
Preparing to unpack .../libpython3.12-minimal_3.12.3-1ubuntu0.8_amd64.deb ...
Unpacking libpython3.12-minimal:amd64 (3.12.3-1ubuntu0.8) ...
Selecting previously unselected package libexpat1:amd64.
Preparing to unpack .../libexpat1_2.6.1-2ubuntu0.3_amd64.deb ...
Unpacking libexpat1:amd64 (2.6.1-2ubuntu0.3) ...
Selecting previously unselected package python3.12-minimal.
Preparing to unpack .../python3.12-minimal_3.12.3-1ubuntu0.8_amd64.deb ...
Unpacking python3.12-minimal (3.12.3-1ubuntu0.8) ...
Setting up libpython3.12-minimal:amd64 (3.12.3-1ubuntu0.8) ...
Setting up libexpat1:amd64 (2.6.1-2ubuntu0.3) ...
Setting up python3.12-minimal (3.12.3-1ubuntu0.8) ...
Selecting previously unselected package python3-minimal.
(Reading database ... 4700 files and directories currently installed.)
Preparing to unpack .../0-python3-minimal_3.12.3-0ubuntu2_amd64.deb ...
Unpacking python3-minimal (3.12.3-0ubuntu2) ...
Selecting previously unselected package media-types.
Preparing to unpack .../1-media-types_10.1.0_all.deb ...
Unpacking media-types (10.1.0) ...
Selecting previously unselected package netbase.
Preparing to unpack .../2-netbase_6.4_all.deb ...
Unpacking netbase (6.4) ...
Selecting previously unselected package tzdata.
Preparing to unpack .../3-tzdata_2025b-0ubuntu0.24.04.1_all.deb ...
Unpacking tzdata (2025b-0ubuntu0.24.04.1) ...
Selecting previously unselected package readline-common.
Preparing to unpack .../4-readline-common_8.2-4build1_all.deb ...
Unpacking readline-common (8.2-4build1) ...
Selecting previously unselected package libreadline8t64:amd64.
Preparing to unpack .../5-libreadline8t64_8.2-4build1_amd64.deb ...
Adding 'diversion of /lib/x86_64-linux-gnu/libhistory.so.8 to /lib/x86_64-linux-gnu/libhistory.so.8.usr-is-merged by libreadline8t64'
Adding 'diversion of /lib/x86_64-linux-gnu/libhistory.so.8.2 to /lib/x86_64-linux-gnu/libhistory.so.8.2.usr-is-merged by libreadline8t64'
Adding 'diversion of /lib/x86_64-linux-gnu/libreadline.so.8 to /lib/x86_64-linux-gnu/libreadline.so.8.usr-is-merged by libreadline8t64'
Adding 'diversion of /lib/x86_64-linux-gnu/libreadline.so.8.2 to /lib/x86_64-linux-gnu/libreadline.so.8.2.usr-is-merged by libreadline8t64'
Unpacking libreadline8t64:amd64 (8.2-4build1) ...
Selecting previously unselected package libsqlite3-0:amd64.
Preparing to unpack .../6-libsqlite3-0_3.45.1-1ubuntu2.5_amd64.deb ...
Unpacking libsqlite3-0:amd64 (3.45.1-1ubuntu2.5) ...
Selecting previously unselected package libpython3.12-stdlib:amd64.
Preparing to unpack .../7-libpython3.12-stdlib_3.12.3-1ubuntu0.8_amd64.deb ...
Unpacking libpython3.12-stdlib:amd64 (3.12.3-1ubuntu0.8) ...
Selecting previously unselected package python3.12.
Preparing to unpack .../8-python3.12_3.12.3-1ubuntu0.8_amd64.deb ...
Unpacking python3.12 (3.12.3-1ubuntu0.8) ...
Selecting previously unselected package libpython3-stdlib:amd64.
Preparing to unpack .../9-libpython3-stdlib_3.12.3-0ubuntu2_amd64.deb ...
Unpacking libpython3-stdlib:amd64 (3.12.3-0ubuntu2) ...
Setting up python3-minimal (3.12.3-0ubuntu2) ...
Selecting previously unselected package python3.
(Reading database ... 5706 files and directories currently installed.)
Preparing to unpack .../python3_3.12.3-0ubuntu2_amd64.deb ...
Unpacking python3 (3.12.3-0ubuntu2) ...
Selecting previously unselected package openssl.
Preparing to unpack .../openssl_3.0.13-0ubuntu3.6_amd64.deb ...
Unpacking openssl (3.0.13-0ubuntu3.6) ...
Selecting previously unselected package ca-certificates.
Preparing to unpack .../ca-certificates_20240203_all.deb ...
Unpacking ca-certificates (20240203) ...
Setting up media-types (10.1.0) ...
Setting up libsqlite3-0:amd64 (3.45.1-1ubuntu2.5) ...
Setting up tzdata (2025b-0ubuntu0.24.04.1) ...
debconf: unable to initialize frontend: Dialog
debconf: (No usable dialog-like program is installed, so the dialog based frontend cannot be used. at /usr/share/perl5/Debconf/FrontEnd/Dialog.pm line 79.)
debconf: falling back to frontend: Readline
debconf: unable to initialize frontend: Readline
debconf: (Can't locate Term/ReadLine.pm in @INC (you may need to install the Term::ReadLine module) (@INC entries checked: /etc/perl /usr/local/lib/x86_64-linux-gnu/perl/5.38.2 /usr/local/share/perl/5.38.2 /usr/lib/x86_64-linux-gnu/perl5/5.38 /usr/share/perl5 /usr/lib/x86_64-linux-gnu/perl-base /usr/lib/x86_64-linux-gnu/perl/5.38 /usr/share/perl/5.38 /usr/local/lib/site_perl) at /usr/share/perl5/Debconf/FrontEnd/Readline.pm line 8.)
debconf: falling back to frontend: Teletype
Configuring tzdata
------------------

Please select the geographic area in which you live. Subsequent configuration
questions will narrow this down by presenting a list of cities, representing
the time zones in which they are located.

  1. Africa      4. Arctic    7. Australia  10. Pacific
  2. America     5. Asia      8. Europe     11. Etc
  3. Antarctica  6. Atlantic  9. Indian     12. Legacy
Geographic area: 

Geographic area: 5

Please select the city or region corresponding to your time zone.

  1. Aden         23. Dili         45. Krasnoyarsk   67. Samarkand
  2. Almaty       24. Dubai        46. Kuala_Lumpur  68. Seoul
  3. Amman        25. Dushanbe     47. Kuching       69. Shanghai
  4. Anadyr       26. Famagusta    48. Kuwait        70. Singapore
  5. Aqtau        27. Gaza         49. Macau         71. Srednekolymsk
  6. Aqtobe       28. Harbin       50. Magadan       72. Taipei
  7. Ashgabat     29. Hebron       51. Makassar      73. Tashkent
  8. Atyrau       30. Ho_Chi_Minh  52. Manila        74. Tbilisi
  9. Baghdad      31. Hong_Kong    53. Muscat        75. Tehran
  10. Bahrain     32. Hovd         54. Nicosia       76. Tel_Aviv
  11. Baku        33. Irkutsk      55. Novokuznetsk  77. Thimphu
  12. Bangkok     34. Istanbul     56. Novosibirsk   78. Tokyo
  13. Barnaul     35. Jakarta      57. Omsk          79. Tomsk
  14. Beirut      36. Jayapura     58. Oral          80. Ulaanbaatar
  15. Bishkek     37. Jerusalem    59. Phnom_Penh    81. Urumqi
  16. Brunei      38. Kabul        60. Pontianak     82. Ust-Nera
  17. Chita       39. Kamchatka    61. Pyongyang     83. Vientiane
  18. Choibalsan  40. Karachi      62. Qatar         84. Vladivostok
  19. Chongqing   41. Kashgar      63. Qostanay      85. Yakutsk
  20. Colombo     42. Kathmandu    64. Qyzylorda     86. Yangon
  21. Damascus    43. Khandyga     65. Riyadh        87. Yekaterinburg
[More] 69

  22. Dhaka       44. Kolkata      66. Sakhalin      88. Yerevan
Time zone: 69


Current default time zone: 'Asia/Shanghai'
Local time is now:      Sat Oct 25 20:23:00 CST 2025.
Universal Time is now:  Sat Oct 25 12:23:00 UTC 2025.
Run 'dpkg-reconfigure tzdata' if you wish to change it.

Setting up netbase (6.4) ...
Setting up openssl (3.0.13-0ubuntu3.6) ...
Setting up readline-common (8.2-4build1) ...
Setting up ca-certificates (20240203) ...
debconf: unable to initialize frontend: Dialog
debconf: (No usable dialog-like program is installed, so the dialog based frontend cannot be used. at /usr/share/perl5/Debconf/FrontEnd/Dialog.pm line 79.)
debconf: falling back to frontend: Readline
debconf: unable to initialize frontend: Readline
debconf: (Can't locate Term/ReadLine.pm in @INC (you may need to install the Term::ReadLine module) (@INC entries checked: /etc/perl /usr/local/lib/x86_64-linux-gnu/perl/5.38.2 /usr/local/share/perl/5.38.2 /usr/lib/x86_64-linux-gnu/perl5/5.38 /usr/share/perl5 /usr/lib/x86_64-linux-gnu/perl-base /usr/lib/x86_64-linux-gnu/perl/5.38 /usr/share/perl/5.38 /usr/local/lib/site_perl) at /usr/share/perl5/Debconf/FrontEnd/Readline.pm line 8.)
debconf: falling back to frontend: Teletype
Updating certificates in /etc/ssl/certs...
146 added, 0 removed; done.
Setting up libreadline8t64:amd64 (8.2-4build1) ...
Setting up libpython3.12-stdlib:amd64 (3.12.3-1ubuntu0.8) ...
Setting up python3.12 (3.12.3-1ubuntu0.8) ...
Setting up libpython3-stdlib:amd64 (3.12.3-0ubuntu2) ...
Setting up python3 (3.12.3-0ubuntu2) ...
running python rtupdate hooks for python3.12...
running python post-rtupdate hooks for python3.12...
Processing triggers for libc-bin (2.39-0ubuntu8.6) ...
Processing triggers for ca-certificates (20240203) ...
Updating certificates in /etc/ssl/certs...
0 added, 0 removed; done.
Running hooks in /etc/ca-certificates/update.d...
done.
root@f3c678f04cee:/# docker cp app.py my_python:/app.py
bash: docker: command not found
root@f3c678f04cee:/# exit
exit
yachao20070113@localhost:~/my-hello-world-project$ docker cp app.py my_python:/app.py
lstat /home/yachao20070113/my-hello-world-project/app.py: no such file or directory
yachao20070113@localhost:~/my-hello-world-project$ # 格式：docker run -d -P -v [本地目录]:[容器内目录] [镜像名] [容器内执行的命令]
docker run -d -P -v $(pwd):/app python:3 python /app/app.py
Unable to find image 'python:3' locally
3: Pulling from library/python
31ecb0fa272d: Pull complete 
795dbedde24d: Pull complete 
6287f334c0e7: Pull complete 
444728a57358: Pull complete 
26dfe2fac1c4: Pull complete 
79d5bd8a8d26: Pull complete 
89d573bf42b3: Pull complete 
Digest: sha256:78ad0471881f0232093c9e6edf58addade7bf106377732e0790c0f0c914b3b7b
Status: Downloaded newer image for python:3
6ce4403067200bc3db11dcaa8d3b6f86ae870298450c0435a06dfe745aaead68
yachao20070113@localhost:~/my-hello-world-project$ docker port 778eee43b980
yachao20070113@localhost:~/my-hello-world-project$ docker logs -f 778eee43b980
root@778eee43b980:/# docker export 778eee43b980 > ubuntu.tar
bash: docker: command not found
root@778eee43b980:/# docker exec -it 778eee43b980 /bin/bash
bash: docker: command not found
achao20070113@localhost:~/my-hello-world-project$ docker ps
CONTAINER ID   IMAGE     COMMAND       CREATED             STATUS             PORTS     NAMES
778eee43b980   ubuntu    "/bin/bash"   About an hour ago   Up About an hour             ubuntu-test
97bc5b3a5db8   ubuntu    "/bin/bash"   About an hour ago   Up About an hour             beautiful_bartik
yachao20070113@localhost:~/my-hello-world-project$  docker inspect  ubuntu-test
[
    {
        "Id": "778eee43b9803f778a073a30b8536c5d493c05cb01c369b0697475bce9c2c976",
        "Created": "2025-10-25T11:19:44.07276706Z",
        "Path": "/bin/bash",
        "Args": [],
        "State": {
            "Status": "running",
            "Running": true,
            "Paused": false,
            "Restarting": false,
            "OOMKilled": false,
            "Dead": false,
            "Pid": 684,
            "ExitCode": 0,
            "Error": "",
            "StartedAt": "2025-10-25T11:22:34.48973207Z",
            "FinishedAt": "2025-10-25T11:22:12.928328133Z"
        },
        "Image": "sha256:66460d557b25769b102175144d538d88219c077c678a49af4afca6fbfc1b5252",
        "ResolvConfPath": "/var/lib/docker/containers/778eee43b9803f778a073a30b8536c5d493c05cb01c369b0697475bce9c2c976/resolv.conf",
        "HostnamePath": "/var/lib/docker/containers/778eee43b9803f778a073a30b8536c5d493c05cb01c369b0697475bce9c2c976/hostname",
        "HostsPath": "/var/lib/docker/containers/778eee43b9803f778a073a30b8536c5d493c05cb01c369b0697475bce9c2c976/hosts",
        "LogPath": "/var/lib/docker/containers/778eee43b9803f778a073a30b8536c5d493c05cb01c369b0697475bce9c2c976/778eee43b9803f778a073a30b8536c5d493c05cb01c369b0697475bce9c2c976-json.log",
        "Name": "/ubuntu-test",
        "RestartCount": 0,
        "Driver": "overlayfs",
        "Platform": "linux",
        "MountLabel": "",
        "ProcessLabel": "",
        "AppArmorProfile": "",
        "ExecIDs": null,
        "HostConfig": {
            "Binds": null,
            "ContainerIDFile": "",
            "LogConfig": {
                "Type": "json-file",
                "Config": {}
            },
            "NetworkMode": "bridge",
            "PortBindings": {},
            "RestartPolicy": {
                "Name": "no",
                "MaximumRetryCount": 0
            },
            "AutoRemove": false,
            "VolumeDriver": "",
            "VolumesFrom": null,
            "ConsoleSize": [
                26,
                79
            ],
            "CapAdd": null,
            "CapDrop": null,
            "CgroupnsMode": "private",
            "Dns": [],
            "DnsOptions": [],
            "DnsSearch": [],
            "ExtraHosts": null,
            "GroupAdd": null,
            "IpcMode": "private",
            "Cgroup": "",
            "Links": null,
            "OomScoreAdj": 0,
            "PidMode": "",
            "Privileged": false,
            "PublishAllPorts": false,
            "ReadonlyRootfs": false,
            "SecurityOpt": null,
            "UTSMode": "",
            "UsernsMode": "",
            "ShmSize": 67108864,
            "Runtime": "runc",
            "Isolation": "",
            "CpuShares": 0,
            "Memory": 0,
            "NanoCpus": 0,
            "CgroupParent": "",
            "BlkioWeight": 0,
            "BlkioWeightDevice": [],
            "BlkioDeviceReadBps": [],
            "BlkioDeviceWriteBps": [],
            "BlkioDeviceReadIOps": [],
            "BlkioDeviceWriteIOps": [],
            "CpuPeriod": 0,
            "CpuQuota": 0,
            "CpuRealtimePeriod": 0,
            "CpuRealtimeRuntime": 0,
            "CpusetCpus": "",
            "CpusetMems": "",
            "Devices": [],
            "DeviceCgroupRules": null,
            "DeviceRequests": null,
            "MemoryReservation": 0,
            "MemorySwap": 0,
            "MemorySwappiness": null,
            "OomKillDisable": null,
            "PidsLimit": null,
            "Ulimits": [],
            "CpuCount": 0,
            "CpuPercent": 0,
            "IOMaximumIOps": 0,
            "IOMaximumBandwidth": 0,
            "MaskedPaths": [
                "/proc/asound",
                "/proc/acpi",
                "/proc/interrupts",
                "/proc/kcore",
                "/proc/keys",
                "/proc/latency_stats",
                "/proc/timer_list",
                "/proc/timer_stats",
                "/proc/sched_debug",
                "/proc/scsi",
                "/sys/firmware",
                "/sys/devices/virtual/powercap"
            ],
            "ReadonlyPaths": [
                "/proc/bus",
                "/proc/fs",
                "/proc/irq",
                "/proc/sys",
                "/proc/sysrq-trigger"
            ]
        },
        "GraphDriver": {
            "Data": null,
            "Name": "overlayfs"
        },
        "Mounts": [],
        "Config": {
            "Hostname": "778eee43b980",
            "Domainname": "",
            "User": "",
            "AttachStdin": false,
            "AttachStdout": false,
            "AttachStderr": false,
            "Tty": true,
            "OpenStdin": true,
            "StdinOnce": false,
            "Env": [
                "PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin"
            ],
            "Cmd": [
                "/bin/bash"
            ],
            "Image": "ubuntu",
            "Volumes": null,
            "WorkingDir": "",
            "Entrypoint": null,
            "OnBuild": null,
            "Labels": {
                "desktop.docker.io/wsl-distro": "Ubuntu",
                "org.opencontainers.image.ref.name": "ubuntu",
                "org.opencontainers.image.version": "24.04"
            }
        },
        "NetworkSettings": {
            "Bridge": "",
            "SandboxID": "a08ef1ea56d68ae238680fe1a8d5729c1362b000e0519f4cca353a59ba0e1281",
            "SandboxKey": "/var/run/docker/netns/a08ef1ea56d6",
            "Ports": {},
            "HairpinMode": false,
            "LinkLocalIPv6Address": "",
            "LinkLocalIPv6PrefixLen": 0,
            "SecondaryIPAddresses": null,
            "SecondaryIPv6Addresses": null,
            "EndpointID": "2d8de9ec0c5f78370a95ef577fe4bf938b7ac145ed1d729c3640b44d6559d608",
            "Gateway": "172.17.0.1",
            "GlobalIPv6Address": "",
            "GlobalIPv6PrefixLen": 0,
            "IPAddress": "172.17.0.3",
            "IPPrefixLen": 16,
            "IPv6Gateway": "",
            "MacAddress": "a6:75:7b:b6:3a:a0",
            "Networks": {
                "bridge": {
                    "IPAMConfig": null,
                    "Links": null,
                    "Aliases": null,
                    "MacAddress": "a6:75:7b:b6:3a:a0",
                    "DriverOpts": null,
                    "GwPriority": 0,
                    "NetworkID": "a70560d0718182f42b13601f451e65a174c2f38232dfbd6fb4f182e080531868",
                    "EndpointID": "2d8de9ec0c5f78370a95ef577fe4bf938b7ac145ed1d729c3640b44d6559d608",
                    "Gateway": "172.17.0.1",
                    "IPAddress": "172.17.0.3",
                    "IPPrefixLen": 16,
                    "IPv6Gateway": "",
                    "GlobalIPv6Address": "",
                    "GlobalIPv6PrefixLen": 0,
                    "DNSNames": null
                }
            }
        },
        "ImageManifestDescriptor": {
            "mediaType": "application/vnd.oci.image.manifest.v1+json",
            "digest": "sha256:d22e4fb389065efa4a61bb36416768698ef6d955fe8a7e0cdb3cd6de80fa7eec",
            "size": 424,
            "annotations": {
                "com.docker.official-images.bashbrew.arch": "amd64",
                "org.opencontainers.image.base.name": "scratch",
                "org.opencontainers.image.created": "2025-10-01T00:00:00Z",
                "org.opencontainers.image.revision": "f5b85bb809ca07067994b7b0ec661a31718d6c75",
                "org.opencontainers.image.source": "https://git.launchpad.net/cloud-images/+oci/ubuntu-base",
                "org.opencontainers.image.url": "https://hub.docker.com/_/ubuntu",
                "org.opencontainers.image.version": "24.04"
            },
            "platform": {
                "architecture": "amd64",
                "os": "linux"
            }
        }
    }
]
yachao20070113@localhost:~/my-hello-world-project$ docker stop ubuntu-test
ubuntu-test
yachao20070113@localhost:~/my-hello-world-project$ 