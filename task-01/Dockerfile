FROM ubuntu:jammy
RUN apt-get update && apt-get -qq -y install curl
RUN curl -LO https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl
RUN chmod +x ./kubectl
RUN mv ./kubectl /usr/local/bin
COPY ./saccount-config /root/.kube/config
CMD ["sleep", "3600"]
