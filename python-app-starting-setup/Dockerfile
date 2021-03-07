# We gonna use an image of python as the base image
FROM python:3

# The base directory in the container
WORKDIR /app

# Copy all the files into the WORKDIR
# COPY <hostfile system> <image/container file system>
COPY . .

# Execute the command python with the script file as arg
# python rng.py
# The difference to run is that this will now not be executed
# when the image is created, but when a container is started based on the image.
CMD [ "python", "rng.py" ]