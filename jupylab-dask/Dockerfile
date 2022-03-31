FROM ejimenezr/jupylab-dev:latest


USER $NB_USER

RUN pip install numpy pandas h5py pillow matplotlib scipy toolz  snakeviz scikit-image dask dask[distributed] 
RUN pip install graphviz bokeh tables fastparquet sklearn
RUN pip install dask_ml

USER root
# python3 setup
RUN apt-get update && apt-get install -y graphviz git
