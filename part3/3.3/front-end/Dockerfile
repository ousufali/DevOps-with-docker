FROM node:12.22


WORKDIR /usr/src/app

COPY . .

RUN npm install


RUN npm run build
RUN npm install -g serve

EXPOSE 5000


RUN useradd newuser1

USER newuser1



CMD ["serve" ,"-s", "-l" ,"5000", "build"]
