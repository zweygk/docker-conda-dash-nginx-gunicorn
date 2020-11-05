FROM continuumio/miniconda3

RUN conda update conda

COPY ./environment.yml /environment.yml
WORKDIR /

RUN conda env create -f ./environment.yml
RUN rm -rf /environment.yml

ENV PATH /opt/conda/envs/myenv/bin:$PATH
ENV CONDA_DEFAULT_ENV myenv
ENV CONDA_PREFIX /opt/conda/envs/myenv
