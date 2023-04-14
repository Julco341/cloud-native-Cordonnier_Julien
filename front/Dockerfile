FROM golang:alpine AS build-stage

WORKDIR /app

RUN go env -w GO111MODULE=off

COPY dispatcher.go .
COPY static ./static

RUN go build -o /docker-gs-ping

FROM build-stage AS run-test-stage

FROM alpine AS build-release-stage

WORKDIR /
COPY static ./static
COPY --from=build-stage /docker-gs-ping /docker-gs-ping

EXPOSE 80

ENTRYPOINT ["/docker-gs-ping"]
