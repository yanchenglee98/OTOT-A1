FROM node:alpine

# Create app directory inside the container
WORKDIR /usr/src/app

# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied 
# where available (npm@5+)
COPY package*.json ./

RUN npm install
# If you are building your code for production
# RUN npm ci --only=production

# Copy the generated modules and all other files to the container
COPY . .

# app is running on port 5000 within the container, so need to expose it
EXPOSE 5000

CMD ["node", "index.js"]
