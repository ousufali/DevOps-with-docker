FROM alpine:3.13 as build-stage


WORKDIR /usr/src/app

COPY . .


RUN apk add --no-cache npm \
    && npm install \
    && npm run build \
    && adduser -D newuser1




FROM node:16-alpine

WORKDIR /app

COPY --from=build-stage /usr/src/app/build ./build
COPY --from=build-stage /etc/passwd /etc/passwd

RUN  npm install -g serve


USER newuser1 

EXPOSE 5000

CMD ["serve" ,"-s", "-l" ,"5000", "build"]


