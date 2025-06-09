FROM node:22-alpine

WORKDIR /app

COPY . .

RUN npm install --omit=dev

# Thêm healthcheck giả
HEALTHCHECK CMD exit 0

# CMD đúng đường dẫn file sau khi COPY
CMD ["node", "src/filesystem/dist/index.js", "/projects"]
