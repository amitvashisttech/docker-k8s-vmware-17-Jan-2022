# Base Image 
FROM ubuntu:16.04 

# Update the APT Repo 
RUN apt-get update 

# Install Apache Packages 
RUN apt-get install apache2 -y 

# Copy Custom Web Page 
COPY index.html /var/www/html/

# Expose Web Port
EXPOSE 80 

# Bring the Apache App UP
CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]
