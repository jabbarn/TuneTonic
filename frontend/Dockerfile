FROM node:latest
LABEL version=1.0

ENV ADB_IP=192.168.1.139
ENV REACT_NATIVE_HOSTNAME=192.168.1.1
EXPOSE 19000 19001

RUN apt-get update -y && apt-get install -y android-tools-adb

WORKDIR /app
COPY package*.json ./
RUN npm i

CMD adb connect $ADB_IP && npm run android
