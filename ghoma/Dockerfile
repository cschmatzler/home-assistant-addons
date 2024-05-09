ARG BUILD_FROM
FROM $BUILD_FROM

ENV LANG C.UTF-8
WORKDIR /ghoma

RUN apk add --no-cache \
  nodejs \
  npm

COPY index.js package.json package-lock.json ./
RUN npm ci

COPY run.sh ./
RUN chmod +x run.sh
