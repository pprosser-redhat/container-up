FROM node:14



ARG TEST
ENV NODE_ENV production
ENV TEST2=value2

WORKDIR /usr/src/app

# Just copy the package.json...
COPY package*.json ./

# so we can cache this layer:
RUN npm install

COPY . .

RUN echo "The port is ${TEST}"
RUN echo "The value is ${TEST2}"

EXPOSE ${TEST}

# command to run on container start
CMD [ "node", "./bin/www" ]
