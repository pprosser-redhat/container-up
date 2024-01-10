FROM node:14

WORKDIR /usr/src/app

ARG PHILPORT
ENV NODE_ENV production
ENV TEST2=value2

# Just copy the package.json...
COPY package*.json ./

# so we can cache this layer:
RUN npm install

COPY . .

RUN echo "The port is $PHILPORT"
RUN echo "The value is $TEST2"

EXPOSE $PHILPORT

# command to run on container start
CMD [ "node", "./bin/www" ]
