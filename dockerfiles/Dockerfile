FROM ubuntu as os
RUN apt update # && apt upgrade -y
RUN apt install -y curl sudo apt-utils ca-certificates gnupg lsb-release
RUN curl -fsSL https://get.docker.com -o get-docker.sh && sh get-docker.sh