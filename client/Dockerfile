FROM node:lts-alpine

# install simple http server for serving static content
RUN npm install -g http-server
WORKDIR /app
COPY package*.json ./
COPY . .
RUN npm install
RUN npm run build
EXPOSE 8080
CMD [ "http-server", "target" ]