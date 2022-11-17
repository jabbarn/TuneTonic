FROM node:16-alpine
LABEL version=1.0

EXPOSE 19000 19001
ENV ADB_IP=192.168.1.139
ENV REACT_NATIVE_HOSTNAME=192.168.1.1

RUN apt-get update && apt-get install android-tools-adb

WORKDIR /app

COPY package.json yarn.lock app.json ./
RUN yarn --network-timeout 100000
CMD adb connect $ADB_IP && yarn run android
