FROM ejimenezr/jupylab-dev:latest


ARG GIT_EMAIL
ARG GIT_NAME
ARG NEW_PASSPHRASE


RUN apt-get  update -y && apt-get install -y openssh-server openssh-client  && apt-get install -y git
RUN mkdir ~/.ssh
RUN echo $GIT_EMAIL && ssh-keygen -t ed25519 -f ~/.ssh/id_ed25519 -C $GIT_EMAIL -N $NEW_PASSPHRASE \
    && eval "$(ssh-agent -s)" && ssh-add ~/.ssh/id_ed25519 

# CMD echo "$GIT_NAME"
# #CMD git config --global user.name $GIT_USER && git config --global user.email $GIT_EMAIL
# 