FROM jupyter/minimal-notebook


COPY ./overrides_jupyterlab.json /opt/conda/share/jupyter/lab/settings/overrides.json

#code formatter
RUN pip install --upgrade jupyterlab && \
    jupyter labextension install @ryantam626/jupyterlab_code_formatter && \
    pip install jupyterlab_code_formatter && \
    jupyter serverextension enable --py jupyterlab_code_formatter && \
    pip install yapf

RUN jupyter labextension install @ryantam626/jupyterlab_sublime

#nbdev
RUN pip install nbdev