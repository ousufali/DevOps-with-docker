FROM node:14.16.1-alpine3.12


WORKDIR /usr/src/app

COPY . .

RUN npm install


RUN npm run build
RUN npm install -g serve

EXPOSE 5000

CMD ["serve" ,"-s", "-l" ,"5000", "build"]
