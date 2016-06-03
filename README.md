ELK docker
==========

Download elk zip files
-------------------

```
wget https://download.elastic.co/logstash/logstash/logstash-2.3.2.tar.gz -P logstash
wget https://download.elastic.co/elasticsearch/release/org/elasticsearch/distribution/zip/elasticsearch/2.3.3/elasticsearch-2.3.3.zip -P elasticsearch
wget https://download.elastic.co/kibana/kibana/kibana-4.5.1-linux-x64.tar.gz -P kibana
```

Run
-------------

```
docker-compose up -d
```
