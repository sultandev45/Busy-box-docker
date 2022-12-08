# Pull the minimal Ubuntu image
FROM ubuntu

RUN apt-get -y update && apt-get -y install busybox
# Copy over the executable file
COPY ./server /home/
# Run the executable file
CMD /home/server
