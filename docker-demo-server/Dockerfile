# image to use
FROM node:carbon

# Create app directory
WORKDIR /usr/src/app

# copies package.json AND package-lock.json using wildcard
COPY package*.json ./

# Install app dependencies
RUN npm install

# Bundle app source
COPY . .

# port app uses 
EXPOSE 8000

# Command to execute to start app
CMD [ "npm", "run", "dev" ]