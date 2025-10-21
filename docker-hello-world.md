yachao20070113@localhost:~/my-hello-world-project$ docker run ubuntu:20.04 /bin/echo "Hello world"
Hello world
yachao20070113@localhost:~/my-hello-world-project$ docker run -i -t ubuntu:20.04 /bin/bash
root@d5ac35c4e6ae:/# cat /proc/version
Linux version 6.6.87.2-microsoft-standard-WSL2 (root@439a258ad544) (gcc (GCC) 11.2.0, GNU ld (GNU Binutils) 2.37) #1 SMP PREEMPT_DYNAMIC Thu Jun  5 18:30:46 UTC 2025
root@d5ac35c4e6ae:/# exit
exit
yachao20070113@localhost:~/my-hello-world-project$ docker run -d ubuntu:15.10 /bin/sh -c "while true; do echo hello world; sleep 1; done"
docker: Error response from daemon: apply layer error for "": failed to extract layer sha256:f121afdbbd5dd49d4a88c402b1a1a4dca39c9ae75ed7f80a29ffd9739fc680a7: NotFound: failed to get reader from content store: content digest sha256:7dcf5a4443927558c6720517b7996d912d98288d6f565e99195d1b72431a38ca: not found

Run 'docker run --help' for more information
yachao20070113@localhost:~/my-hello-world-project$ docker run -d ubuntu:20.04 /bin/sh -c "while true; do echo hello world; sleep 1; done"
78a9b42ef3d7aadcb519b52663b1f8fcc19b2627b506ae7935b39e4f4bdfe40e
yachao20070113@localhost:~/my-hello-world-project$  docker ps
CONTAINER ID   IMAGE          COMMAND                  CREATED          STATUS          PORTS     NAMES
78a9b42ef3d7   ubuntu:20.04   "/bin/sh -c 'while t…"   18 seconds ago   Up 17 seconds             nervous_curie
8110b24fdd0e   ubuntu:20.04   "/bin/bash"              5 minutes ago    Up 5 minutes              nifty_jang
59e16c7c33da   ubuntu:20.04   "/bin/sh -c 'while t…"   9 minutes ago    Up 9 minutes              wonderful_wu
83eb43cec122   ubuntu:20.04   "/bin/sh -c 'while t…"   14 minutes ago   Up 14 minutes             relaxed_archimedes
yachao20070113@localhost:~/my-hello-world-project$ docker logs
docker: 'docker logs' requires 1 argument

Usage:  docker logs [OPTIONS] CONTAINER

Run 'docker logs --help' for more information
yachao20070113@localhost:~/my-hello-world-project$ 
yachao20070113@localhost:~/my-hello-world-project$ docker logs nervous_curie
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
hello world
yachao20070113@localhost:~/my-hello-world-project$ docker stop nervous_curie

nervous_curie
yachao20070113@localhost:~/my-hello-world-project$ 
yachao20070113@localhost:~/my-hello-world-project$ docker ps
CONTAINER ID   IMAGE          COMMAND                  CREATED          STATUS          PORTS     NAMES
8110b24fdd0e   ubuntu:20.04   "/bin/bash"              9 minutes ago    Up 9 minutes              nifty_jang
59e16c7c33da   ubuntu:20.04   "/bin/sh -c 'while t…"   12 minutes ago   Up 12 minutes             wonderful_wu
83eb43cec122   ubuntu:20.04   "/bin/sh -c 'while t…"   17 minutes ago   Up 17 minutes             relaxed_archimedes