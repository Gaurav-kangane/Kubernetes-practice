# Use lightweight Node.js image
FROM node:18-alpine

# Set working directory
WORKDIR /app

# Copy dependency files first (for caching)
COPY package*.json ./

# Install dependencies
RUN npm install --production

# Copy application code
COPY server.js .

# Expose application port
EXPOSE 3000

# Start the app
CMD ["node", "server.js"]
