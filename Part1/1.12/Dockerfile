FROM node:16-alpine

EXPOSE 5000

WORKDIR /usr/src/app

# Copy package.json and package-lock.json to install dependencies
COPY package*.json ./

# Install dependencies
RUN npm install

COPY . .

# Build the static files for production
RUN npm run build

# Install "serve" globally to serve the static files
RUN npm install -g serve

# Command to serve the static files on port 5000
CMD ["serve", "-s", "-l", "5000", "build"]