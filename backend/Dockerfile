FROM node:20.18.0-alpine
EXPOSE 8080
ENV DB_HOST="mysql"

RUN addgroup -S expense && adduser -S expense -G expense && \
    mkdir /opt/server && \
    chown -R expense:expense /opt/server
WORKDIR /opt/server

COPY package.json .
COPY *.js .
RUN npm install
USER expense

CMD ["node", "index.js"]


# Before Best Practices its 1.1 GB image
# FROM node:20 
# EXPOSE 8080
# ENV DB_HOST="mysql"
# RUN mkdir /opt/server
# WORKDIR /opt/server
# COPY package.json .
# COPY *.js .
# RUN npm install
# CMD ["node", "index.js"]