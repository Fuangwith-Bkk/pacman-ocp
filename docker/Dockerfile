# FROM node:boron
FROM registry.access.redhat.com/ubi8/nodejs-12:latest

MAINTAINER Ivan Font <ifont@redhat.com>

# Create app directory
WORKDIR /usr/src/app

# Clone game source code
# RUN git clone https://github.com/font/pacman.git .
RUN git clone https://github.com/Fuangwith-Bkk/pacman-ocp.git .


# Install app dependencies
RUN npm install

# Expose port 8080
EXPOSE 8080

# Run container
CMD ["npm", "start"]
