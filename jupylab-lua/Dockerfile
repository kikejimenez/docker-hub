FROM ejimenezr/jupylab-dev:latest


RUN conda update -y -n base conda && conda install mamba -n base -c conda-forge 

RUN mamba install xeus-lua jupyterlab -y -c conda-forge