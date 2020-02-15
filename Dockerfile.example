FROM [image name]

# Create app directory
WORKDIR /usr/src/app

# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied

COPY package*.json ./

RUN npm install

# Bundle app source
COPY . .

EXPOSE 8000

# Command to execute to start app
CMD [ "node", "server.js" ]