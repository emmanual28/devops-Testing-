FROM node:20-alpine

WORKDIR /app 

# Copy package.json first for dependency installation
COPY package*.json ./

RUN npm install 

# Copy the rest of your app files
COPY . .

EXPOSE 5001 

CMD ["node","server.js"]
