FROM ubuntu

MAINTAINER Gianluca Damaggio <damaggiogianluca@gmail.com>

RUN apt update && \
apt -y upgrade   

RUN apt-get update && \
apt-get install -y git && \
apt-get install -y build-essential && \
apt-get install wget


RUN wget --quiet https://repo.anaconda.com/archive/Anaconda3-2020.02-Linux-x86_64.sh -O ~/anaconda3.sh && \
/bin/bash ~/anaconda3.sh -b -p /opt/conda && \
rm ~/anaconda3.sh && \
ln -s /opt/conda/etc/profile.d/conda.sh /etc/profile.d/conda.sh && \
echo ". /opt/conda/etc/profile.d/conda.sh" >> ~/.bashrc && \
echo "conda activate" >> ~/.bashrc

ENV PATH="/opt/conda/bin:${PATH}"

RUN pip install glob2
RUN pip install argparse
RUN pip install subprocess32
RUN pip install random2
RUN pip install pandas
RUN conda install -c bioconda tabix

RUN git clone https://github.com/ezcn/grep.git

