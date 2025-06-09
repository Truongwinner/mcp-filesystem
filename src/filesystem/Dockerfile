FROM node:22-alpine

WORKDIR /app

# Copy package files
COPY package*.json ./

# Install dependencies
RUN npm ci --only=production

# Copy source code
COPY . .

# Build TypeScript (nếu cần)
RUN npm run build

# Không có HEALTHCHECK

CMD ["node", "dist/index.js", "/projects"]
