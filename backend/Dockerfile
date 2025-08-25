# Base build image
FROM node:18-alpine as build

# Set working directory
WORKDIR /app

# Copy only the dependency files
COPY package*.json ./

# Install only production dependencies
RUN npm install --production

# Copy the rest of the app
COPY . .

# Final minimal runtime image
FROM node:18-alpine

# Set working directory
WORKDIR /app

# Copy only built app and dependencies
COPY --from=build /app /app

# Use a non-root user for security
RUN addgroup -S appgroup && adduser -S appuser -G appgroup
USER appuser

# Expose application port
EXPOSE 4000

# Start the application
CMD ["npm", "start"]

