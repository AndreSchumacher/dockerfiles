# Shark worker
FROM shark-base:0.7.0
MAINTAINER Matt Massie massie@berkeley.edu

# Setup a volume for data
VOLUME ["/data"]

# Instead of using a random port, bind the worker to a specific port
# Note: Here we assume the virtual bridge is used!
ENV SPARK_WORKER_PORT 8888
#EXPOSE 8888

# Add run script
ADD files /root/shark_worker_files

# Add the entrypoint script for the worker
ENTRYPOINT ["/root/shark_worker_files/default_cmd"]
