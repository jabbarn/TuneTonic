FROM --platform=$BUILDPLATFORM node:lts AS dev-envs

WORKDIR /code
COPY package.json /code/package.json
COPY package-lock.json /code/package-lock.json

RUN npm ci
COPY . /code

ENV CI=true
ENV PORT=8080

CMD [ "npm", "start" ]
