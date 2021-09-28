# conversao-temperatura - Docker process

## Installation

First, create a folder, and start by cloning the repository into this new folder:

```
https://github.com/eferroni/conversao-temperatura.git
```

- Create the container from the image on docker hub

```
docker container run -d -p 8080:8080 eduferroni/conversao-temperatura:v1
```

- Go to your browser and enter the url:
```
localhost:8080
```

## Dockerfile
```
FROM node:14.17.5
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
EXPOSE 8080
CMD ["node", "server.js"]
```
