FROM node:18
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
EXPOSE 5000
CMD ["npm", "start"]

# FROM node:18.9.1

# WORKDIR /app

# Copy package.json  .

# RUN npm install

# COPY . .

# EXPOSE 5000

# CMD ["npm","start"]
