# Use the official Node.js image as the base image

FROM node:lts-alpine


# Set the working directory inside the container

WORKDIR /app


# Copy package.json and package-lock.json to the working directory

COPY package*.json ./


# Install dependencies using npm

RUN npm install


# Copy the rest of the application code to the working directory

COPY . .


# Expose port 8081 (change this to your desired port)

EXPOSE 8081


# Start the Node.js application

CMD ["node", "index.js"]
