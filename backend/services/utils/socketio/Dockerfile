FROM node:16.20.2-alpine

# 设置构建参数
ARG HTTP_PROXY
ARG HTTPS_PROXY

# 设置环境变量
ENV HTTP_PROXY=$HTTP_PROXY
ENV HTTPS_PROXY=$HTTPS_PROXY
WORKDIR /app
COPY ./package*.json ./

RUN npm install

COPY ./ .

CMD ["node", "server.js"]