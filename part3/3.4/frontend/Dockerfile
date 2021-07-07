FROM alpine:3.13


WORKDIR /usr/src/app

COPY . .
EXPOSE 5000

RUN apk add --no-cache npm \
    && npm install \
    && npm run build \
    && npm install -g serve \
    && adduser -D newuser1


USER newuser1


CMD ["serve" ,"-s", "-l" ,"5000", "build"]
