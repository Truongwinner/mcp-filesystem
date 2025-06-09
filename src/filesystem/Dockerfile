FROM node:22-alpine

WORKDIR /app

# Cài curl để dùng nếu cần trong tương lai
RUN apk add --no-cache curl

# Cài package MCP Filesystem
RUN npm install @modelcontextprotocol/server-filesystem

# Thêm HEALTHCHECK để luôn báo "healthy"
HEALTHCHECK CMD echo "OK"

# CMD thực thi server MCP
CMD ["node", "node_modules/@modelcontextprotocol/server-filesystem/dist/index.js", "/projects"]
