# Use Node base image
FROM node:18

# Create app directory inside container
WORKDIR /app

# Copy package.json first
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy full project
COPY . .

# Expose port (change if your app uses different port)
EXPOSE 3001

# Start app
CMD ["node", "src/index.js"]
