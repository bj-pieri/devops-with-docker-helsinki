```bash
❯ docker run -d --name exercise devopsdockeruh/simple-web-service:alpine
Unable to find image 'devopsdockeruh/simple-web-service:alpine' locally
alpine: Pulling from devopsdockeruh/simple-web-service
ba3557a56b15: Pull complete
1dace236434b: Pull complete
4f4fb700ef54: Pull complete
Digest: sha256:dd4d367476f86b7d7579d3379fe446ae5dfce25480903fb0966fc2e5257e0543
Status: Downloaded newer image for devopsdockeruh/simple-web-service:alpine
a9d83e025a7db57b2861f33010efc7bb66988dd4eea32eda1228d1f56ff127d2
❯ docker exec -it exercise sh
/usr/src/app # tail -f ./text.log
2023-05-31 00:22:03 +0000 UTC
2023-05-31 00:22:05 +0000 UTC
2023-05-31 00:22:07 +0000 UTC
2023-05-31 00:22:09 +0000 UTC
Secret message is: 'You can find the source code here: https://github.com/docker-hy'


COMPARING THE TWO IMAGES BELLOW:

❯ docker image ls
REPOSITORY                          TAG       IMAGE ID       CREATED       SIZE
ubuntu                              latest    3b418d7b466a   5 weeks ago   77.8MB
devopsdockeruh/simple-web-service   ubuntu    4e3362e907d5   2 years ago   83MB
devopsdockeruh/simple-web-service   alpine    fd312adc88e0   2 years ago   15.7MB

