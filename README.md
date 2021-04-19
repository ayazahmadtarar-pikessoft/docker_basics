# docker_basics

Docker version

docker run hello-world

docker run hello-world ls | Docker run hello-world echo who am I

docker ps

docker run busybox ping google.com
docker ps --all
Docker run = docker create +docker start
docker create hello-world
docker start -a e423c2609f35ca56b65f5e7fb2650e11fc53b1512d826571299044472900533e

docker start e423c2609f35ca56b65f5e7fb2650e11fc53b1512d826571299044472900533e
Docker start -a e423c2609f35
Docker start -a e423c2609f35 echo hi # not allowed
docker system prune
docker logs d9fac763444497a52b2a80eace01368cec0f8f73d6b962f1c7901a3fbe40f646

docker stop 3c828039f658
docker kill 3c828039f658
Docker run redis
docker exec -it f826acfd476c redis-cli
docker exec -i -t # input + text show pretty
docker exec -it f826acfd476c sh
Use exec instead of docker run -it busybox sh 
docker build .

Docker file 
# Instruction argument
FROM alpine

RUN apk add --update redis

CMD ["redis-server"]
