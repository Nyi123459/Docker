# fill in the blanks to dockerize this node app
FROM node:23-alpine3.20

EXPOSE 3000 

RUN apk add --no-cache tini

WORKDIR /usr/src/app

COPY package.json package.lock.json* ./

RUN npm install && npm cache clean --force

COPY . .

ENTRYPOINT ["tini", "--"]

CMD ["node", "app.js"]
