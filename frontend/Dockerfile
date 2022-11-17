FROM node:latest
LABEL version=1.0

ENV ADB_IP=192.168.1.139
ENV REACT_NATIVE_HOSTNAME=192.168.1.1

RUN apt-get update -y && ap-get install -y android-tools-adb


EXPOSE 19000 19001

RUN yarn
CMD adb connect $ADB_IP && yarn run android
