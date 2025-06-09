FROM node:22.12-alpine AS builder
WORKDIR /app

COPY . .

RUN npm install
RUN npm run build

FROM node:22-alpine AS release
WORKDIR /app
COPY --from=builder /app /app

CMD ["node", "dist/index.js", "/projects"]
