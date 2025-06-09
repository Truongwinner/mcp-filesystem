FROM node:22-alpine

WORKDIR /app

COPY . .                    # copy toàn bộ mã nguồn repo

RUN npm install            # cài dependencies
RUN npm run build          # build TypeScript nếu cần

HEALTHCHECK NONE           # disable healthcheck (Coolify)

CMD ["node", "dist/index.js", "/projects"]  # chạy server với repo riêng
