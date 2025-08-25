# Stage 1: Build the frontend
FROM node:18-alpine AS build

# Set working directory
WORKDIR /app

# Copy only package files first to cache dependencies
COPY package*.json ./

# Install dependencies
RUN npm ci --silent

# Copy the rest of the application code
COPY . .

# Build the app
RUN npm run build

# Stage 2: Serve with Nginx
FROM nginx:stable-alpine AS production

# Remove default Nginx static files
RUN rm -rf /usr/share/nginx/html/*

# Copy built frontend from previous stage
COPY --from=build /app/dist /usr/share/nginx/html

# Permissions (good for non-root access scenarios)
RUN chmod -R 755 /usr/share/nginx/html

# Expose port
EXPOSE 80

# Start Nginx
CMD ["nginx", "-g", "daemon off;"]


