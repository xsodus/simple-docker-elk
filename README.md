# Simple Docker ELK
A simple ELK (Elasticsearch, Logstash and Kibana) docker compose template. I just created this project to learn how to setup and run this stack.

#### Prerequisites
- Docker Desktop installed and running
- At least 4GB of available RAM
- Docker Desktop configured with sufficient resources (recommended: 4GB RAM, 2 CPU cores)

#### Setup
You'll need to install Docker first.
Then setup all config files for each service at `config` directory
You can see all details in these URLs.

https://hub.docker.com/_/elasticsearch

https://hub.docker.com/_/logstash/

https://hub.docker.com/_/kibana/


#### Run
You can run this stack by these commands:

**Option 1: Run in detached mode (recommended)**
```bash
$ docker-compose up -d
```

**Option 2: Run with logs visible**
```bash
$ docker-compose up
```

**To stop the stack:**
```bash
$ docker-compose down
```

**To clean up and restart fresh:**
```bash
$ docker-compose down -v
$ docker-compose up -d
```

#### Access Services
After running the command, you should be able to access these services at the following URLs:
- Kibana : http://localhost:5601
- Elasticsearch : http://localhost:9200

#### Initial Setup
For first time setup in Kibana:
1. Go to http://localhost:5601
2. Navigate to Stack Management > Data Views (formerly Index Management)
3. Create a new data view with pattern `logstash-*`
4. Set `@timestamp` as the time field

#### Troubleshooting
If you encounter "read-only file system" errors:
1. Ensure Docker Desktop has sufficient permissions
2. Try restarting Docker Desktop
3. Clean up Docker system: `docker system prune -f`
4. Ensure you have enough disk space

If services fail to start:
1. Check Docker logs: `docker-compose logs`
2. Ensure ports 5601, 9200, 9600, and 5044 are not in use
3. Increase Docker Desktop memory allocation to at least 4GB

#### Verification
If all services are working correctly, you should see a sample message which is delivered by `heartbeat` every 5 seconds in the Kibana Discover tab.
