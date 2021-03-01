# We gonna use an image of node js as the base image
FROM node:14

# The base directory in the container
WORKDIR /app

# Copy the package.json into the WORKDIR
COPY package.json .

# execute npm install to install al the dependencies required
RUN npm install

# Copy all the files into the WORKDIR
COPY . .

# Expose the same port that the app expose
EXPOSE 80

# Execute the command node with the app file as arg
# node app.mjs
CMD [ "node", "server.js" ]