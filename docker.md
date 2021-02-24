# Docker

## Kill running docker container

```bash
$ docker kill (docker ps -q)
```

## Share files between container and host

```bash
$ docker run -v /home/waynee95/Public:/mnt/Public
```

This will mount `/home/waynee95/Public` to `/mnt/Public` inside the docker container.
