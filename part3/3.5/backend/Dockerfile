FROM golang:alpine

WORKDIR /usr/src/app

COPY . .


ENV REQUEST_ORIGIN=http://localhost:5000
EXPOSE 8080

RUN go build \
    && adduser -D newuser1


USER newuser1

CMD ["./server"]
