# Use Node image for frontend build
FROM node:18

# Set working directory
WORKDIR /app

# Copy frontend package.json and lock file
COPY package*.json ./

# Install frontend dependencies
RUN npm install

# Copy all frontend source files
COPY . .

# Expose port for frontend
EXPOSE 3000

# Start the React frontend
CMD ["npm", "start"]
