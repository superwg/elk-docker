#FROM ubuntu:14.04
FROM java:8
COPY sources.list /etc/apt/sources.list
RUN useradd -ms /bin/bash elk
RUN apt-get update
RUN apt-get install -y unzip
COPY logstash-2.3.2.tar.gz /opt/
RUN cd /opt && tar -zxvf /opt/logstash-2.3.2.tar.gz
COPY logstash-syslog.conf /opt/
RUN chown -R elk /opt/logstash-2.3.2
#RUN echo 'network.host: 0.0.0.0' >> /opt/logstash-2.3.2/config/elasticsearch.yml
#USER elk
EXPOSE 5000
CMD /opt/logstash-2.3.2/bin/logstash -f /opt/logstash-syslog.conf
