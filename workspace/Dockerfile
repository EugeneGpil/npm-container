FROM ubuntu:20.04

ARG NODE_VERSION=14.18.0
RUN apt-get update && \
    apt-get install curl -y && \
    curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh | bash && \
    export NVM_DIR="$HOME/.nvm" && \
    . $NVM_DIR/nvm.sh && \
    nvm install ${NODE_VERSION} && \
    curl -fsSL https://code-server.dev/install.sh | sh && \
    apt-get install git -y && \
    apt-get install nano -y

ARG NODE_VERSION=14.18.0
ENV PATH /root/.nvm/versions/node/v${NODE_VERSION}/bin:${PATH}
ARG VUE_CLI_VERSION=4.5.14
RUN npm config set user 0 && \
    npm config set unsafe-perm true && \
    npm i -g @vue/cli@${VUE_CLI_VERSION}
