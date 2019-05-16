# Specify a base image
FROM node:alpine
# Specify a work directory
WORKDIR /usr/app
# Copy files
COPY ./package.json ./
# Install some dependencies
RUN npm install
# Copy changed files
COPY ./ ./
# Default command
CMD ["npm", "start"]