FROM gitpod/workspace-full
USER root

RUN npm install -g @bazel/bazelisk
RUN npm install -g @bazel/ibazel

RUN apt-get update && \
    apt-get install -y -qq wget

USER gitpod

ENV CONDA_DIR /home/gitpod/conda
ENV PATH=$CONDA_DIR/bin:$PATH
RUN wget --quiet https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda.sh && \
     /bin/bash ~/miniconda.sh -b -p /home/gitpod/conda

RUN /home/gitpod/conda/bin/conda install jupyter keras tensorflow -y --quiet && \
    pip3 install tensorflow

RUN pip3 install dash && \
    pip3 install dash-daq && \
    pip3 install pandas matplotlib