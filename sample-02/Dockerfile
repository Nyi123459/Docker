FROM node:23-alpine

EXPOSE 3000

WORKDIR /usr/src/app

COPY package.json package-lock.json* ./ 

RUN apk add --update curl

RUN npm install && npm cache clean --force

COPY . .

CMD [ "node", "./bin/www" ]
