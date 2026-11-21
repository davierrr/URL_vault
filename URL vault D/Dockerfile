# Use official Node.js 20 LTS lightweight image
FROM node:20-alpine

# Set working directory inside container
WORKDIR /app

# Copy package dependency definitions
COPY package*.json ./

# Install project dependencies
RUN npm install

# Copy application source code
COPY . .

# Build the React frontend into static production files (dist/)
RUN npm run build

# Configure production environment
ENV NODE_ENV=production
ENV PORT=10000

# Expose Render standard service port
EXPOSE 10000

# Start production full-stack server
CMD ["npm", "start"]
