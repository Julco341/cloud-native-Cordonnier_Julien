# How to launch image.

## Build image

```bash
$ docker build -f Dockerfile . -t web-server-test
```

## Run image
```bash
$ docker run -p 8000:80 web-server-test
```

## Test

Go to : http://<ip>:8000