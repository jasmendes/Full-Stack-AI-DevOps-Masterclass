FROM node:22-alpine

WORKDIR /app

# Copy package files first
COPY package*.json ./

# Install only production dependencies
RUN npm ci --omit=dev

# Copy application
COPY . .

EXPOSE 3000

CMD ["node", "index.js"]