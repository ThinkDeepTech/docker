FROM haydenmcp/environment:development-ubuntu-nodejs-0.0.2

ARG GIT_AUTHOR_NAME
ARG GIT_AUTHOR_EMAIL

ENV GIT_AUTHOR_NAME=$GIT_AUTHOR_NAME
ENV GIT_AUTHOR_EMAIL=$GIT_AUTHOR_EMAIL


# Environment Setup/Configuration
USER root

# Perform System Update
RUN apt-get update && apt-get upgrade -y

# Git
RUN apt-get install git -y

# VS Code
ADD vscode.deb .
RUN apt install -y ./vscode.deb
RUN rm vscode.deb
RUN apt-get install apt-transport-https -y
RUN apt-get update
RUN apt-get install -y code

# User Configuration
USER developer

RUN mkdir ~/code
WORKDIR ~/code

CMD ["/bin/bash"]