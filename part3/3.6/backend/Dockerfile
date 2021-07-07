FROM golang:alpine  as build-stage

WORKDIR /usr/src/app

COPY . .



RUN go build \
    && adduser -D newuser1




FROM alpine:latest

COPY --from=build-stage /usr/src/app/server ./server
COPY --from=build-stage /etc/passwd /etc/passwd
ENV REQUEST_ORIGIN=http://localhost:5000
EXPOSE 8080


USER newuser1

CMD ["./server"]
