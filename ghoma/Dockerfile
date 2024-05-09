FROM oven/bun:1.1.7-alpine

WORKDIR /ghoma

ADD index.js package.json bun.lockb .
RUN bun i

EXPOSE 3000 4196

CMD ["bun", "run" "index.js"]
