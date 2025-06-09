FROM node:22-alpine

WORKDIR /app

# Copy toàn bộ source code (bao gồm dist/) đã build sẵn
COPY . .

# Cài dependencies nhưng không chạy prepare script
RUN npm set-script prepare "" && npm install --omit=dev

# Disable healthcheck nếu muốn tránh log Unhealthy
HEALTHCHECK CMD ["true"]

# CMD khởi chạy server từ dist đã build sẵn
CMD ["node", "dist/index.js", "/projects"]
