ARG BUILD_FROM
FROM $BUILD_FROM

ENV LANG C.UTF-8
WORKDIR /

RUN apk add --no-cache \
  nodejs \
  npm

COPY index.js package.json package-lock.json ./
RUN npm ci

EXPOSE 3000 4196

COPY rootfs /
