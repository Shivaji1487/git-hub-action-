# Lightweight Nginx image
FROM nginx:alpine

# HTML file ko Nginx default public directory mein copy karein
COPY index.html /usr/share/nginx/html/index.html

# Port expose karein
EXPOSE 80

# Nginx foreground mein run karein
CMD ["nginx", "-g", "daemon off;"]