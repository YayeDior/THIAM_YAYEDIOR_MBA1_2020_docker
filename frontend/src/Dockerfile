FROM node:8.7.0-alpine

RUN mkdir -p /srv/app/fr-shoshin-admin-client
WORKDIR //srv/app/fr-shoshin-admin-client

COPY package.json /srv/app/fr-shoshin-admin-client
COPY package-lock.json /srv/app/fr-shoshin-admin-client

RUN npm install 

COPY . /srv/app/fr-shoshin-admin-client


CMD [ "npm", "start" ]