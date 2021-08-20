#FROM node:boron
FROM registry.access.redhat.com/ubi8/nodejs-12:latest

# Create app directory
WORKDIR /usr/src/app

COPY package*.json ./

# Install app dependencies
RUN npm install

COPY . .

# Expose port 8080
EXPOSE 8080

# Run container
CMD ["npm", "start"]







