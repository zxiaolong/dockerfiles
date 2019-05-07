FROM ubuntu:bionic

COPY Makefile /sphinx
COPY source /sphinx
RUN apt-get update
RUN apt-get install -y iputils-ping net-tools iproute2 && \
apt-get install -y vim openssh-server

RUN apt-get install -y python-pip

RUN pip install sphinx
RUN apt-get install -y texlive-full latexmk
RUN pip install sphinxcontrib-svg2pdfconverter
RUn apt-get install -y inkscape

