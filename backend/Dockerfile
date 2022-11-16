FROM node:16-alpine AS dev-envs

WORKDIR /app

COPY package*.json ./

RUN npm i

COPY . .

ENV PORT=8080

EXPOSE 8080

CMD ["npm", "run", "start:dev"]
