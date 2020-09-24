FROM node:8.7.0-alpine

WORKDIR /usr/src/app

COPY package*.json  ./
RUN npm install 

COPY . . 
EXPOSE 8081

CMD [ "npm", "start" ]
