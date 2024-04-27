# Use the official Ubuntu 20.04 LTS image
FROM ubuntu:22.04

COPY . /var/www/html/

# Update package lists and install Apache
RUN apt-get update \
    && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends apache2 \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

# Set the Apache environment variables
ENV APACHE_RUN_USER www-data
ENV APACHE_RUN_GROUP www-data
ENV APACHE_LOG_DIR /var/log/apache2
ENV APACHE_PID_FILE /var/run/apache2/apache2.pid
ENV APACHE_RUN_DIR /var/run/apache2
ENV APACHE_LOCK_DIR /var/lock/apache2

# Expose port 80
EXPOSE 80

# Start Apache in the foreground
CMD ["apache2", "-D", "FOREGROUND"]

