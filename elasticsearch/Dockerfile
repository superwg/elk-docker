#FROM ubuntu:14.04
FROM java:8
COPY sources.list /etc/apt/sources.list
RUN useradd -ms /bin/bash elk
RUN apt-get update
RUN apt-get install -y unzip
COPY elasticsearch-2.3.3.zip /opt/
RUN cd /opt && unzip /opt/elasticsearch-2.3.3.zip && chown -R elk /opt/elasticsearch-2.3.3
RUN echo 'network.host: 0.0.0.0' >> /opt/elasticsearch-2.3.3/config/elasticsearch.yml
USER elk
EXPOSE 9200
CMD /opt/elasticsearch-2.3.3/bin/elasticsearch
