FROM ubuntu:jammy

ENV LANG C.UTF-8
ENV TZ=Etc/UTC

ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get -y update \
    && apt-get -y install software-properties-common \
    && add-apt-repository -y --update ppa:ansible/ansible \
    && apt-get -y install ansible \
    && apt-get -y install curl \
    && apt-get autoremove -y \
    && apt-get clean -y
ADD https://astral.sh/uv/install.sh /install.sh
RUN chmod -R 655 /install.sh && /install.sh && rm /install.sh