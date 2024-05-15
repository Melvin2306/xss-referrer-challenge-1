FROM node:alpine as base

WORKDIR /app

COPY package.json package-lock.json ./

RUN rm -rf node_modules && yarn install --frozen-lockfile && yarn cache clean

COPY . .

CMD ["node", "./server.js"]

EXPOSE 80