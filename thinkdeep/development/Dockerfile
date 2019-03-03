FROM haydenmcp/environment:development-ubuntu-nodejs-0.0.1

ENV GIT_AUTHOR_NAME $GIT_AUTHOR_NAME
ENV GIT_AUTHOR_EMAIL $GIT_AUTHOR_EMAIL

RUN sudo apt-get update && sudo apt-get upgrade -y
RUN sudo apt-get install git -y

RUN git config --global user.name $GIT_AUTHOR_NAME && git config --global user.email GIT_AUTHOR_EMAIL
