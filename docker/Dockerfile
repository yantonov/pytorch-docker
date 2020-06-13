FROM yantonov/anaconda3

MAINTAINER Yury Antonov <yantonov@yandex.ru>

RUN conda config --add channels conda-forge
RUN conda config --add channels pytorch

ADD files/* /
RUN pip install -r /requirements.txt
