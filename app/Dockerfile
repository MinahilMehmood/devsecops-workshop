FROM node:18-alpine

# Set working directory
WORKDIR /app

# Copy dependency files first (better caching)
COPY package*.json ./

# Install only production dependencies
RUN npm install --production

# Copy application code
COPY . .

# App runs on port 3000
EXPOSE 3000

# Start the app
CMD ["node", "index.js"]
