# We gonna use an image of node js as the base image
FROM node:14

# The base directory in the container
WORKDIR /app

# Copy all the files into the WORKDIR
# COPY <hostfile system> <image/container file system>
COPY . .

# execute npm install to install al the dependencies required
RUN npm install

# Expose the same port that the app expose
EXPOSE 80

# Execute the command node with the app file as arg
# node app.mjs
CMD [ "node", "server.js" ]