from ubuntu:latest

ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get -qq update
RUN apt-get install -y texlive-xetex \
    vim

ENTRYPOINT ["/bin/bash"]
