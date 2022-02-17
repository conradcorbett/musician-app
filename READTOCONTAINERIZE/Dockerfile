#use latest alpine linux image
FROM alpine:latest

#install nodejs and npm
RUN apk add --no-cache nodejs npm

#set directory to where the app is
WORKDIR /github/musician-app

COPY . /github/musician-app

RUN npm install express --save

EXPOSE 3001

ENTRYPOINT ["node"]

CMD ["app.js"]