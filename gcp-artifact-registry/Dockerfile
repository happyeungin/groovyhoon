FROM --platform=linux/amd64 ubuntu:22.04
FROM python:3.9
# Install pytorch cuda 11.7 from pytorch cuda 11.3 docker image
FROM pytorch/pytorch:1.11.0-cuda11.3-cudnn8-runtime

# Define work dir is /code
WORKDIR /code

RUN apt-get -y update
RUN apt-get install -y --no-install-recommends python3-pip

# Install opencv-python
# Docker may miss some default opencv packages
RUN apt-get update && apt-get install -y python3-opencv
RUN pip install opencv-python

RUN pip install \
argcomplete>=1.9.4 \
poetry==1.1.14 \
jupyterlab==3.3.0 \
accelerate==0.20.3 \
annotated-types==0.5.0 \
anyio==3.7.1 \
beautifulsoup4==4.12.2 \
certifi==2023.5.7 \
charset-normalizer==3.2.0 \
click==8.1.4 \
colorama==0.4.6 \
controlnet-aux==0.0.6 \
diffusers==0.18.1 \
einops==0.6.1 \
exceptiongroup==1.1.2 \
fastapi==0.100.0 \
filelock==3.12.2 \
fsspec==2023.6.0 \
gdown==4.7.1 \
h11==0.14.0 \
huggingface-hub==0.16.4 \
idna==3.4 \
imageio==2.31.1 \
importlib-metadata==6.8.0 \
Jinja2==3.1.2 \
kornia==0.6.12 \
lazy_loader==0.3 \
MarkupSafe==2.1.3 \
mpmath==1.3.0 \
mypy-extensions==1.0.0 \
networkx==3.1 \
numpy==1.24.4 \
opencv-python==4.8.0.74 \
packaging==23.1 \
Pillow==10.0.0 \
psutil==5.9.5 \
pydantic==2.0.2 \
pydantic_core==2.1.2 \
pyre-extensions==0.0.29 \
pyvirtualcam==0.10.2 \
PyWavelets==1.4.1 \
PyYAML==6.0 \
regex==2023.6.3 \
requests==2.31.0 \
safetensors==0.3.1 \
scikit-image==0.21.0 \
scipy==1.10.1 \
six==1.16.0 \
sniffio==1.3.0 \
soupsieve==2.4.1 \
starlette==0.27.0 \
sympy==1.12 \
tifffile==2023.7.4 \
timm==0.9.2 \
tokenizers==0.13.3 \
tqdm==4.65.0 \
transformers==4.30.2 \
transparent-background==1.2.4 \
typing-inspect==0.9.0 \
typing_extensions==4.7.1 \
urllib3==2.0.3 \
uvicorn==0.22.0 \
xformers==0.0.20 \
zipp==3.16.0


# Create a link that points to the right python bin directory
RUN ln -s /usr/bin/python3.9 /usr/bin/python
