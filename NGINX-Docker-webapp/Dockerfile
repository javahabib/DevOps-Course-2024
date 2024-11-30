# Use an Nginx base image to serve the HTML file
FROM nginx:alpine

# Copy the HTML file to the default Nginx directory
COPY index.html /usr/share/nginx/html/index.html

# Expose port 80 so it can be accessed externally
EXPOSE 80