FROM ubuntu as os
RUN apt update && apt upgrade -y
# required packages
RUN apt install -y curl sudo wget ca-certificates gnupg lsb-release software-properties-common
# docker engine install
RUN curl -fsSL https://get.docker.com -o get-docker.sh && sh get-docker.sh
# terraform install
RUN wget -O- https://apt.releases.hashicorp.com/gpg | \
    gpg --dearmor | \
    tee /usr/share/keyrings/hashicorp-archive-keyring.gpg \
    echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] \
    https://apt.releases.hashicorp.com $(lsb_release -cs) main" | \
    sudo tee /etc/apt/sources.list.d/hashicorp.list \
    apt upate && apt install terraform