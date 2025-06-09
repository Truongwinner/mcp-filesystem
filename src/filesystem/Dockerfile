FROM node:22-alpine

WORKDIR /app

COPY . .

# Bỏ cài đặt & build vì dist đã build sẵn
# Tắt healthcheck vì không cần dùng
HEALTHCHECK NONE

# Chạy file dist đã build sẵn
CMD ["node", "src/filesystem/dist/index.js", "/projects"]
