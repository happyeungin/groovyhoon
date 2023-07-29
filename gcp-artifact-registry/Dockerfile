FROM python:3.9

# Install pytorch cuda 11.7 from pytorch cuda 11.3 docker image
FROM pytorch/pytorch:1.11.0-cuda11.3-cudnn8-runtime

# Define work dir is /code
WORKDIR /code

RUN apt-get -y update
RUN apt-get install -y --no-install-recommends \
python3-pip \

# Install opencv-python
# Docker may miss some default opencv packages
RUN apt-get update && apt-get install -y python3-opencv
RUN pip install opencv-python

RUN pip install \
argcomplete>=1.9.4 \
poetry==1.1.14 \
jupyterlab==3.3.0

# Create a link that points to the right python bin directory
RUN ln -s /usr/bin/python3.9 /usr/bin/python
