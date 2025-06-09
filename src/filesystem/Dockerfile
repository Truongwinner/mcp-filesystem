FROM node:22-alpine

WORKDIR /app

# Cài curl để tránh lỗi healthcheck trong Coolify
RUN apk add --no-cache curl

RUN npm install @modelcontextprotocol/server-filesystem

CMD ["node", "node_modules/@modelcontextprotocol/server-filesystem/dist/index.js", "/projects"]

HEALTHCHECK CMD curl --silent --fail http://localhost || exit 0
