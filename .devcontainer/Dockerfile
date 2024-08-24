FROM ubuntu:latest

ARG UNAME
ARG UID
ARG GID

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update \
&& apt-get install -y --no-install-recommends \
build-essential \
sudo \
curl \
wget \
git \
&& apt-get clean  \
&& apt-get autoremove -y \
&& rm -rf /var/lib/apt/lists/*

RUN useradd --shell /bin/bash --uid $UID --non-unique --create-home $UNAME
RUN groupmod --gid $GID --non-unique $UNAME
