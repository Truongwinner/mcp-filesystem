FROM node:22-alpine

WORKDIR /app

# Cài đặt package MCP Filesystem từ NPM
RUN npm install @modelcontextprotocol/server-filesystem

# CMD thực thi server MCP
CMD ["node", "node_modules/@modelcontextprotocol/server-filesystem/dist/index.js", "/projects"]
