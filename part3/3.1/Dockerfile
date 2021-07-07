FROM node:12.22

WORKDIR /usr/src/app

COPY . .


RUN npm install
RUN npm run build
RUN npm install -g serve

EXPOSE 5000

CMD  ["serve" , "-s", "build" , "-l", "4000"]
