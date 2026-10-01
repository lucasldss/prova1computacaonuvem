# prova1computacaonuvem
cat > index.html <<'EOF'

<title>Atendimento</title>
Atendimento disponivel

EOF docker run -d --name atendimento -p 8082:80 nginx:alpine Unable to find image 'nginx:alpine' locally alpine: Pulling from library/nginx e2d96531ba9c: Pull complete d9aae54b5831: Pull complete 6c53d0b2a666: Pull complete 745dfb2690dd: Pull complete 9a9a644fdd6a: Pull complete 64c81944980fe: Pull complete e76228b47809: Pull complete e72112c14215: Pull complete Digest: sha256:df22ld836e1754089190208cee7eedad94f233197056426 eda74a3ab1abeac2 Status: Downloaded newer image for nginx:alpine bfbf56c7b5abd24b352db0ba5666910d29df7844ff024dcd876d79a56235 e1 root@ubuntu:~$ docker cp index.html atendimento:/usr/share/nginx/html/index.html Successfully copied 2.05kB to atendimento:/usr/share/nginx/html/index.html root@ubuntu:~$ docker ps CONTAINER ID IMAGE STATUS COMMAND PORTS CREATED NAMES bfbf56c7b5ab nginx:alpine "/docker-entrypoint..." About a minute ago Up About a minute 0.0.0.0:8082->80/tcp, [::] 082->80/tcp atendimento root@ubuntu:~$ curl http://localhost:8082 <title>Atendimento</title>
Atendimento disponível

root@ubuntu:~$
