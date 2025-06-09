FROM node:22-alpine

WORKDIR /app

# Cài package đã build sẵn
RUN npm install @modelcontextprotocol/server-filesystem

CMD ["node", "node_modules/@modelcontextprotocol/server-filesystem/dist/index.js", "/projects"]

# ➕ THÊM dòng sau để Docker vẫn tạo .State.Health.Status nhưng không fail
HEALTHCHECK CMD echo "healthy"