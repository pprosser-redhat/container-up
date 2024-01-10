FROM node:14

WORKDIR /usr/src/app

ARG PHILPORT=8080
ENV NODE_ENV production

# Just copy the package.json...
COPY package*.json ./

# so we can cache this layer:
RUN npm install

COPY . .

RUN echo 'The port is ${PHILPORT}'

EXPOSE ${PHILPORT}

# command to run on container start
CMD [ "node", "./bin/www" ]
