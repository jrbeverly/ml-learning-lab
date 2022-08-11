FROM gitpod/workspace-full
USER root

RUN npm install -g @bazel/bazelisk
RUN npm install -g @bazel/ibazel

RUN apt update -y && apt upgrade -y && apt-get install -y -qq wget
RUN pip install pipenv

USER gitpod

# ENV CONDA_DIR /home/gitpod/conda
# ENV PATH=$CONDA_DIR/bin:$PATH
# RUN wget --quiet https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda.sh && \
#      /bin/bash ~/miniconda.sh -b -p /home/gitpod/conda

# RUN /home/gitpod/conda/bin/conda install jupyter keras tensorflow -y --quiet
# RUN pip3 install dash dash-daq pandas matplotlib scikit-learn
