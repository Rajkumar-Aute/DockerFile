FROM ubuntu as os
RUN apt update && apt upgrade -y
# required packages
RUN apt install -y curl sudo wget ca-certificates gnupg lsb-release software-properties-common unzip
# docker engine install
RUN curl -fsSL https://get.docker.com -o get-docker.sh && sh get-docker.sh
# terraform install
RUN wget https://releases.hashicorp.com/terraform/1.2.9/terraform_1.2.9_linux_amd64.zip \
    unzip terraform_1.0.7_linux_amd64.zip \
    mv terraform /usr/local/bin/ \
    rm terraform*.zip