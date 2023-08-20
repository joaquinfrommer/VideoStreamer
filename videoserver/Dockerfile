FROM ubuntu:latest
WORKDIR /stream
RUN mkdir /stream/hls
RUN mkdir /stream/dash
RUN mkdir /web
RUN apt-get update -y
RUN apt install nginx -y
RUN apt-get install libnginx-mod-rtmp -y --option=Dpkg::Options::=--force-confdef
COPY nginx.conf /etc/nginx/nginx.conf
COPY entrypoint.sh /stream/entrypoint.sh
ENTRYPOINT bash /stream/entrypoint.sh
