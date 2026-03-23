FROM node:latest

# Create app directory
WORKDIR /app

RUN npm install

# Copy your JS file
COPY src/index.js .


# Expose port (change if needed)
EXPOSE 3002

# Run the app
CMD ["node", "index.js"]
