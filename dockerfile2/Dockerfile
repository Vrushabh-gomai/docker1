# Use an official Apache image as base
FROM httpd:latest

# Label for identifying the maintainer of this Dockerfile
LABEL maintainer="vrushabh gomai <vrushabhgomai11@gmail.com>"

# (Optional) Set environment variables, if needed
ENV APACHE_LOG_DIR /var/log/apache2
ENV APACHE_RUN_USER www-data
ENV APACHE_RUN_GROUP www-data
ENV APACHE_PID_FILE /var/run/apache2/apache2.pid
ENV APACHE_RUN_DIR /var/run/apache2
ENV APACHE_LOCK_DIR /var/lock/apache2

# (Optional) Expose ports, if needed
EXPOSE 80

# (Optional) Start Apache when container starts
CMD ["httpd", "-D", "FOREGROUND"]
