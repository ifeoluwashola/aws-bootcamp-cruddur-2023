#Pulling base Image
FROM node:16.18

#Setting Enviroment Variable
ENV PORT=3000

#Copy the project directory
COPY . /frontend-react-js

#Set work directory
WORKDIR /frontend-react-js

#Install npm
RUN npm install

#Exposing port
EXPOSE ${PORT}

#Run the np, & start command to start the react.js app in the container
CMD ["npm", "start"]