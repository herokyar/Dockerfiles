FROM debian

LABEL maintainer=@joshuacook

ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update --fix-missing && \
	apt-get install -y  \
	wget bzip2 ca-certificates \
	libglib2.0-0 libxext6 libsm6 libxrender1

RUN  echo 'export PATH=/opt/conda/bin:$PATH' > /etc/profile.d/conda.sh \
  wget -c https://repo.continuum.io/miniconda/Miniconda3-4.3.11-Linux-x86_64.sh \
    /bin/bash Miniconda3-4.3.11-Linux-x86_64.sh -bfp /usr/local/ \
	rm -rf Miniconda3-4.3.11-Linux-x86_64.sh

ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
ENV PATH /opt/conda/bin:$PATH





