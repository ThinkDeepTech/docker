FROM haydenmcp/environment:development-ubuntu-nodejs-0.0.2

ARG GIT_AUTHOR_NAME
ARG GIT_AUTHOR_EMAIL
ARG SSH_KEY

ENV GIT_AUTHOR_NAME=${GIT_AUTHOR_NAME}
ENV GIT_AUTHOR_EMAIL=${GIT_AUTHOR_EMAIL}

# Environment Setup/Configuration
USER root

# Perform System Update
RUN apt-get update && apt-get upgrade -y

# Git
RUN apt-get install git -y

# User Configuration
USER developer

RUN mkdir ~/code
WORKDIR ~/code

COPY ${SSH_KEY} /tmp/
RUN ssh-agent /tmp
RUN ["git", "clone", "git@github.com:ThinkDeepTech/thinkdeep.git"]
RUN rm /tmp/id_rsa



CMD ["/bin/bash"]