# Set the base image to Ubuntu
FROM    node:alpine

# File Author / Maintainer
MAINTAINER Wu xiaojiang

# Install nodemon
RUN npm install -g nodemon

# Provides cached layer for node_modules
ADD package.json /tmp/package.json
RUN cd /tmp && npm install express 
RUN npm install redis
run npm install ip
RUN mkdir -p /src && cp -a /tmp/node_modules /src/

# Define working directory
WORKDIR /src
ADD . /src

# Expose port
EXPOSE  8080

# Run app using nodemon
CMD ["nodemon", "/src/index.js"]
