# Backend: Node.js + TypeScript
FROM node:20-alpine

WORKDIR /app

# Copy dependencies first to use Docker layer cache
COPY package*.json ./
RUN npm ci

# Copy backend sources and compile TypeScript
COPY . .
RUN npm run build

EXPOSE 4001
CMD ["npm", "run", "serve"]
