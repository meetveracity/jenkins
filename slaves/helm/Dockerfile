FROM jenkins/jnlp-slave:3.27-1-alpine

USER root

# Install curl
RUN apk add --no-cache curl

# Install Helm
RUN curl -LO https://git.io/get_helm.sh; \
    chmod 700 get_helm.sh; \
    ./get_helm.sh

# Install kubectl
RUN curl -LO https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl; \
    chmod +x ./kubectl; \
    mv ./kubectl /usr/local/bin/kubectl

USER jenkins