FROM yantonov/anaconda3:2020.11

MAINTAINER Yury Antonov <1390348+yantonov@users.noreply.github.com>

RUN conda config --add channels conda-forge
RUN conda config --add channels pytorch

RUN apt-get update && \
    # required for twisted (gcc is required)
    apt-get install -y build-essential && \

    # opencv-python
    apt-get install -y ffmpeg libsm6 libxext6 && \

    # typically used in some notebooks
    apt-get install -y wget && \
    apt-get clean

ADD files/* /

RUN pip install --upgrade pip

RUN pip install -r /requirements.txt
