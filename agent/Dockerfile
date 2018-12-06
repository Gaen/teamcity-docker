FROM jetbrains/teamcity-minimal-agent:latest

RUN apt-get update

# Install git for agent-side checkout
RUN apt-get install -yq git

# Install python for building nodejs
RUN apt-get install -yq python3.6

RUN apt-get clean

SHELL ["/bin/bash", "-c"]

ENV NVM_DIR=/nvm
RUN mkdir "$NVM_DIR"
RUN curl -s -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash
RUN . "$NVM_DIR/nvm.sh" && command -v nvm

SHELL ["/bin/sh", "-c"]