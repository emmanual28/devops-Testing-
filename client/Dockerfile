FROM node:20-alpine

WORKDIR /app

# Install dependencies
COPY package*.json ./
RUN npm install

# Copy project files
COPY . .
 

ARG VITE_API_URL 
ENV VITE_API_URL = $VITE_API_URL


# Build Vite for production
RUN npm run build

# Install serve to serve production build
RUN npm install -g serve

# Expose port
EXPOSE 5173

# Start production server
CMD ["serve", "-s", "dist", "-l", "5173"]
