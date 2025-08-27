FROM node:22-alpine

# create app directory
WORKDIR /app

# copy package.json & package-lock.json first (for better caching)
COPY package*.json ./

# install dependencies
RUN npm install

# copy rest of the source code
COPY . .

# expose a port if your app listens on it
EXPOSE 3000

# start the app
CMD ["node", "index.js"]

