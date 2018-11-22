# Specify a base image
FROM node:alpine

# Only execute actions in working directory
# so we don't overwrite anything in base image
WORKDIR /usr/app
# File system img doesn't have access to anything on disk 
# Since npm install only depends on package.json
COPY ./package.json ./
# Install dependencies
RUN npm install
# now only changing package.json will affect npm install cache
# we can change index.js and we won't invalidate npm cache
COPY ./ ./

# Default command
CMD ["npm", "start"]