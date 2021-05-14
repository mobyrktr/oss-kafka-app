FROM node:16.1-alpine3.13

WORKDIR /app

COPY package* ./
RUN npm install

COPY . ./
ENV WAIT_VERSION 2.7.2
ADD https://github.com/ufoscout/docker-compose-wait/releases/download/$WAIT_VERSION/wait /wait
RUN chmod +x /wait

CMD ["node", "index.js"]