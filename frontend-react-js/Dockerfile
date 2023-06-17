#Pulling base Image
#FROM node:16.18

#Setting Enviroment Variable
#ENV PORT=3000

#Copy the project directory
#COPY . /frontend-react-js

#Set work directory
#WORKDIR /frontend-react-js

#Install npm
#RUN npm install

#Exposing port
#EXPOSE ${PORT}

#Run the np, & start command to start the react.js app in the container
#CMD ["npm", "start"]


# Use an official Node.js runtime as a parent image
FROM node:16.18 AS builder

# Set the working directory to /app
WORKDIR /frontend-react-js

# Copy the package.json and package-lock.json files to the container
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the app source code to the container
COPY . .

# Build the app for production
RUN npm run build

# Use a smaller, production-ready base image
FROM node:16-alpine

# Set the working directory to /app
WORKDIR /frontend-react-js

# Copy the package.json and package-lock.json files to the container
COPY package*.json ./

# Install only production dependencies
RUN npm install --only=production

# Copy the app source code to the container
COPY --from=builder /frontend-react-js/build ./build

# Set environment variable for port
ENV PORT=3000

# Run as non-root user
RUN useradd -m react-user
USER react-user

# Expose port
EXPOSE ${PORT}

# Start the app
CMD ["npm", "start"]
