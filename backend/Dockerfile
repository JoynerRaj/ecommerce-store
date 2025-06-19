# Use official Node.js image
FROM node:18

# Create app directory
WORKDIR /app

# Copy package.json and package-lock.json
COPY package*.json ./

# Install backend dependencies
RUN npm install

# Copy the rest of the backend source code
COPY . .

# Expose backend port
EXPOSE 5000

# Set environment variable (you can override in docker-compose or CLI)
ENV PORT=5000

# Start the backend
CMD ["node", "app.js"]
