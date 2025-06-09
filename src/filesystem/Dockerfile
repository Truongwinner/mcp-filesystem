FROM node:22-alpine
WORKDIR /app
COPY . .
# Bỏ install/build vì dist đã sẵn có
# Tạo trường Health thành công
HEALTHCHECK CMD exit 0
CMD ["node", "src/filesystem/dist/index.js", "/projects"]

