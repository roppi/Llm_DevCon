FROM nvidia/cuda:12.3.1-base-ubuntu22.04

# Update packages
RUN apt update && apt upgrade -y

# Install basics
RUN apt install -y sudo wget git git-lfs

# Install Development tools
RUN apt install -y python3 python3-pip

# Update pip
RUN pip3 install --no-cache-dir -U pip

# Install pip packages
RUN pip install --no-cache-dir \
  git+https://github.com/huggingface/transformers \
  torch torchvision torchaudio


# Set `DEVCONTAINER` environment variable to help with orientation
ENV DEVCONTAINER=true