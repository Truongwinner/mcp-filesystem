FROM node:22-alpine

WORKDIR /app

# Copy toàn bộ source từ GitHub
COPY . .

# Cài đặt production dependencies (nếu có package-lock.json thì dùng thêm)
RUN npm install --omit=dev

# Tắt healthcheck
HEALTHCHECK CMD ["true"]

# Chạy từ build đã có sẵn
CMD ["node", "dist/index.js", "/projects"]
