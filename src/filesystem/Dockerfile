FROM node:22-alpine

WORKDIR /app

COPY . .

# Cài thêm typescript và shx để build
RUN npm install -g typescript shx

RUN npm install --omit=dev

HEALTHCHECK CMD exit 0

CMD ["node", "src/filesystem/dist/index.js", "/projects"]
