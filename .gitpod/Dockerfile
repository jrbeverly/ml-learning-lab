FROM gitpod/workspace-full
USER root

RUN npm install -g @bazel/bazelisk
RUN npm install -g @bazel/ibazel

RUN apt update -y && apt upgrade -y && apt-get install -y -qq wget nvidia-cuda-toolkit
RUN pip install pipenv

USER gitpod

