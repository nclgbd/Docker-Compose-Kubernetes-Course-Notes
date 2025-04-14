# Use the official Node.js image as the base image
FROM node:23
# Set the working directory in the container to /app
WORKDIR /app
COPY package.json /app
RUN npm install
# Copy all files from the current directory to /app in the folder in the container. This only works because we changed the working directory to /app
COPY . ./
# Expose port 80 to the outside world. This is the port that the Node.js application will listen on.
EXPOSE 80
# The above instructions are for the build stage. The following instructions are for the run stage.
CMD ["node", "server.js"]