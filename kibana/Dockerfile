#FROM ubuntu:14.04
FROM java:8
#COPY sources.list /etc/apt/sources.list
#RUN useradd -ms /bin/bash elk
COPY kibana-4.5.1-linux-x64.tar.gz /opt/
RUN cd /opt && tar zxvf kibana-4.5.1-linux-x64.tar.gz
EXPOSE 5601
#CMD echo "elasticsearch.url: http://${ES_PORT_9200_TCP_ADDR}:9200" | tee -a /opt/kibana-4.5.1-linux-x64/config/kibana.yml && /opt/kibana-4.5.1-linux-x64/bin/kibana
CMD echo "elasticsearch.url: http://es:9200" | tee -a /opt/kibana-4.5.1-linux-x64/config/kibana.yml && /opt/kibana-4.5.1-linux-x64/bin/kibana
