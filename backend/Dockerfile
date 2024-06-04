# Base image
FROM node

# Create app directory
WORKDIR /usr/src/app

# Install PM2 globally
RUN npm install pm2 -g

# Copy package.json and package-lock.json (or yarn.lock)
COPY package*.json ./

# Install app dependencies
RUN npm install

# Bundle app source
COPY . .

# Expose the port the app runs on
EXPOSE 3000

# Define the command to run the app using PM2
CMD ["pm2-runtime", "start", "index.js"]
