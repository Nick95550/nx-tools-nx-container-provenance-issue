# Use Node.js official image
FROM node:20-alpine

# Set working directory
WORKDIR /app

# Copy built application files
COPY dist/index.js .
COPY dist/lib/ ./lib/

# Create non-root user
RUN addgroup -g 1001 -S nodejs
RUN adduser -S nodejs -u 1001

# Change ownership of the app directory
RUN chown -R nodejs:nodejs /app
USER nodejs

# Expose port (if needed for future web app)
EXPOSE 3000

# Start the application
CMD ["node", "index.js"]