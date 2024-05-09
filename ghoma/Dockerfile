ARG BUILD_FROM
FROM $BUILD_FROM

ENV LANG C.UTF-8
SHELL ["/bin/bash", "-o", "pipefail", "-c"]
WORKDIR /ghoma

RUN apk add --no-cache \
  nodejs \
  npm

COPY index.js package.json package-lock.json ./
RUN npm ci

COPY run.sh /
RUN chmod a+x /run.sh

CMD [ "/run.sh" ]
