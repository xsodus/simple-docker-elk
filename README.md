# Docker-ELK
A simple ELK (Elasticsearch, Logstash and Kibana) docker compose template.

#### Setup
You'll need to install docker first.
Then setup all config files for each service at `config` directory
You can see all details in these URLs.
https://hub.docker.com/_/elasticsearch
https://hub.docker.com/_/logstash/
https://hub.docker.com/_/kibana/


#### Run
You can run this stack by this command.
```
  $ docker-compose up
```
After run the command, you should be able to access these services following URLs
- Kibana : http://localhost:5601

For first time, you should create a new index (logstash-*) on Management page.

- Elasticsearch : http://localhost:9200

If all services are working correctly, you should see a sample message which is delivered by `heartbeat` every 5 seconds.
