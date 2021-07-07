FROM golang:1.16

WORKDIR /usr/src/app

COPY . .


ENV REQUEST_ORIGIN=http://localhost:5000
RUN go build

EXPOSE 8080

RUN useradd -m newuser1

USER newuser1



CMD ["./server"]
