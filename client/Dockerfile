FROM node:20-alpine

WORKDIR /app

# Install dependencies
COPY package*.json ./
RUN npm install

# Copy all project files
COPY . .

# Build Vite
RUN npm run dev

# Expose Vite preview port
EXPOSE 5173

# Start the Vite preview server
CMD ["npm", "run", "preview"]
