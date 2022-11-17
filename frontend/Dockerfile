FROM node:16-alpine
LABEL version=1.0

ENV ADB_IP=192.168.1.139
ENV REACT_NATIVE_HOSTNAME=192.168.1.1

RUN apk update -y && apk add -y android-tools-adb

WORKDIR /app
COPY package*.json ./

EXPOSE 19000 19001

RUN yarn
CMD adb connect $ADB_IP && yarn run android
