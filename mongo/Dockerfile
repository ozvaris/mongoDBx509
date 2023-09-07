# Use the official MongoDB Docker image as base
FROM mongo:latest

# Port for MongoDB to run on
EXPOSE 27017

# Copy certificates to the container
COPY ./crt/server.pem /etc/ssl
COPY ./crt/client.pem /etc/ssl
COPY ./crt/ca.crt /etc/ssl


# Copy the configuration file to the container
COPY mongod.conf /etc/mongod.conf

RUN echo "********************************************************"

# Start MongoDB with custom configuration
CMD ["mongod", "--config", "/etc/mongod.conf"]
