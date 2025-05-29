# Stage 1: Build
FROM node:18 AS builder
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
RUN npm run build

# Stage 2: Serve
FROM nginx:stable-alpine
COPY --from=builder /app/dist /usr/share/nginx/html
COPY nginx.conf /etc/nginx/conf.d/default.conf
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]




# Build stage
# FROM node:18.9.1 as builder

# WORKDIR /app
# COPY package*.json ./
# RUN npm install
# COPY . .
# RUN npm run build

# # Production image
# FROM nginx:alpine
# COPY --from=builder /app/dist /usr/share/nginx/html

# # Optional: Custom nginx config
# COPY nginx.conf /etc/nginx/conf.d/default.conf

# EXPOSE 80
# CMD ["nginx", "-g", "daemon off;"]




# FROM node:18.9.1

# WORKDIR /app

# Copy package.json  .

# RUN npm install

# COPY . .

# EXPOSE 5173

# CMD ["npm","run","dev", "--", "--host"]
