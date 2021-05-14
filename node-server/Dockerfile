FROM node:latest
WORKDIR /app

# Copy both package-lock.json and package.json
# We are doing this first to cache the docker layers: https://nodejs.org/en/docs/guides/nodejs-docker-webapp/
COPY package*.json .
RUN npm install

COPY . .
EXPOSE 3000
CMD [ "node", "server.js" ]