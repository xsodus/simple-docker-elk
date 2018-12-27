# Docker-ELK
A simple ELK (Elasticsearch, Logstash and Kibana) docker compose template.

#### Setup
You'll need to install docker first.
Then setup all config files for each service at `config` directory

#### Run
You can run this stack by this command.
```
  $ docker-compose up
```
After run the command, you should be able to access these services following URLs
- Kibana : http://localhost:5601

For first time, you shold create a new index (logstash-*) on Management page.

- Elasticsearch : http://localhost:9200
