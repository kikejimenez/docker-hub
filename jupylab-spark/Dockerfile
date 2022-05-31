FROM jupyter/all-spark-notebook:31b807ec9e83



USER $NB_USER

#upgrade jupyterlab
RUN pip install --upgrade jupyterlab 

#nbdev
RUN pip install nbdev twine

#user settings
USER root

ENV NB_UID=$NB_UID \
    NB_GID=$NB_GID
ADD ./user-settings/.jupyter /home/$NB_USER/.jupyter
RUN chown -R $NB_UID:$NB_GID /home/$NB_USER/.jupyter
