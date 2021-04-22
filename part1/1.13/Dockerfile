FROM golang:1.16

WORKDIR /usr/src/app

COPY . .
RUN go build

EXPOSE 8080

ENV REQUEST_ORIGIN=https://example.com


CMD ["./server"]
