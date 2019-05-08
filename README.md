## scala-sbt

This is a light version of scala and sbt image for docker.

## How to use

You can pull it from docker hub:

`docker pull danhack/scala-sbt`

Or you can add it to your docker compose:

```
services:
  sbt:
    image: danhack/scala-sbt
    stdin_open: true
    tty: true
    entrypoint: sbt
    volumes:
      - $PWD:/root
      - m2repo:/home/user/.m2
      - ivy2:/home/user/.ivy2
    ports:
      - "9000:9000"
```

DockerHub: https://hub.docker.com/r/danhack/scala-sbt

## TODO

 - Implement another openjdk image
