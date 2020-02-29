FROM debian:buster-slim

RUN apt update && \
    apt-get install --yes freerdp2-x11

ENTRYPOINT ["xfreerdp"]
