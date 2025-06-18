# backend/Dockerfile
FROM node:18

# Install build tools and Python
RUN apt-get update && \
    apt-get install -y python3 make g++ && \
    ln -s /usr/bin/python3 /usr/bin/python && \
    rm -rf /var/lib/apt/lists/*

WORKDIR /app

COPY package*.json ./

# Install node modules with compatibility
RUN npm install --legacy-peer-deps

COPY . .

EXPOSE 5000

CMD ["npm", "start"]
