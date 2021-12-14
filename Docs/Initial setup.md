# Introduction to Prometheus and Grafana - Session/Workshop

# Prerequisite
- Docker
- Git

# Installation
- Clone the git repo to your workstation
  `git clone http://github.com/naveenkumarsp/promstack` 
- Open command prompt or powershell console and change the working directory to cloned repo path in your workstation
- Ensure docker for desktop is running by issuing command `docker version`

# Deploy the prometheus stack
A docker-compose file is written which uses the configurations defined in config directory. 
To deploy prometheus stack on docker container, issue command `docker-compose up -d`.

# Destroy the prometheus stack
To destroy the stack run command `docker-compose down`

# Endpoints exposed by prometheus stack
- Prometheus         : http://localhost:9090
- Grafana            : http://localhost:3000
- Alertmanager       : http://localhost:9093
- Couchbase exporter : http://localhost:9091/metrics
- Node Exporter      : http://localhost:9100/metrics
- collectd exporter  : http://localhost:9103/metrics