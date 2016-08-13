FROM ubuntu:16.04 
MAINTAINER iwatobipen <seritaka@gmail.com>
RUN apt-get -y update && apt-get -y install wget
RUN apt-get -y install bzip2
RUN apt-get -y install git-all
RUN apt-get -y install libfreetype6-dev libxft-dev
RUN wget http://repo.continuum.io/archive/Anaconda3-4.1.1-Linux-x86_64.sh
RUN bash ./Anaconda3-4.1.1-Linux-x86_64.sh -b -p /opt/conda 
RUN rm ./Anaconda3-4.1.1-Linux-x86_64.sh
ENV PATH /bin:/usr/bin:/opt/conda/bin:PATH
RUN conda install -y -c rdkit rdkit=2016.03.3
RUN pip install seaborn
RUN conda install -y -c conda-forge keras=1.0.7

CMD /bin/bash
