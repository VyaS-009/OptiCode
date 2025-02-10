# Use an official Node.js runtime as the base image
FROM node:18

# Set the working directory in the container
WORKDIR /app

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install --legacy-peer-deps


# Copy the rest of the frontend code
COPY . .

# Build the Next.js app
RUN npm run build

# Expose the port your frontend runs on (e.g., 3000)
EXPOSE 3000

# Command to run your frontend application
CMD ["npm", "run", "dev"]