# ベースイメージ
FROM node:16-alpine3.15

# Create app directory
WORKDIR /app

# Install app dependencies (package.json and package-lock.json)
COPY package*.json ./
RUN apk update
RUN apk add lsof
RUN npm install
RUN npm install axios
RUN npm install -g npm
RUN npm install -g @vue/cli@3.9.3
RUN npm install -g @vue/cli-init
RUN vue init webpack . 

# Bundle app source (server.js)
COPY . .

# Listen port
EXPOSE 8080