FROM node:16-alpine

# set our node environment, either development or production
# defaults to production, compose overrides this to development on build and run
ARG NODE_ENV=production
ENV NODE_ENV $NODE_ENV

WORKDIR /app

COPY package*.json ./

# default to port 19006 for node, and 19001 and 19002 (tests) for debug
ARG PORT=19006
ENV PORT $PORT
EXPOSE $PORT 19001 19002

# install global packages
ENV NPM_CONFIG_PREFIX=/home/node/.npm-global
ENV PATH /home/node/.npm-global/bin:$PATH

CMD npm install

# copy in our source code last, as it changes the most
# for development, we bind mount volumes; comment out for production
# COPY ./react_native_app .

ENTRYPOINT ["npm", "run"]
CMD ["start"]
