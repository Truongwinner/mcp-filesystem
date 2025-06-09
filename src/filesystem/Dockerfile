FROM node:22-alpine

WORKDIR /app

# Copy toàn bộ source từ GitHub repo của Sếp
COPY . .

# Cài đặt dependencies
RUN npm install

# Biên dịch TypeScript
RUN npm run build

# Vô hiệu hóa healthcheck bằng cách trả về luôn true
HEALTHCHECK CMD [ "true" ]

# Chạy server MCP từ build
CMD ["node", "dist/index.js", "/projects"]
