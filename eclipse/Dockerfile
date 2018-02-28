# Run Eclipse in a container

# $ docker build -t eclipse .
#
# $ docker run -d \
#	    -v /tmp/.X11-unix:/tmp/.X11-unix \
#	    -e DISPLAY=unix$DISPLAY \
#	    --name eclipse \
#       eclipse
#
FROM java

LABEL maintainer "Vineet Palan <vineetpalan@gmail.com>"

ARG ECLIPSE_URL='http://tiny.cc/eclipsefordocker'

RUN curl $ECLIPSE_URL | tar -xvz -C /home

ENTRYPOINT ["/home/eclipse/eclipse"]
