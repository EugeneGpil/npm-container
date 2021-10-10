FROM ubuntu:20.04

ARG NODE_VERSION=14.18.0
RUN apt-get update && \
    apt-get install curl -y && \
    curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh | bash && \
    export NVM_DIR="$HOME/.nvm" && \
    . $NVM_DIR/nvm.sh && \
    nvm install ${NODE_VERSION} && \
    curl -fsSL https://code-server.dev/install.sh | sh
