# Introduction to Prometheus and Grafana - Session/Workshop

# Prerequisite
- Docker
- Git

## Installation
- Clone the git repo to your workstation
  `git clone http://github.com/naveenkumarsp/promstack` 
- Open command prompt or powershell console and change the working directory to cloned repo path in your workstation
- Ensure docker for desktop is running by issuing command `docker version`

### Deploy the prometheus stack
A docker-compose file is written which uses the configurations defined in config directory. 
To deploy prometheus stack on docker container, issue command `docker-compose up -d`.

### Endpoints exposed by prometheus stack
- Prometheus         : http://localhost:9090
- Grafana            : http://localhost:3000
- Alertmanager       : http://localhost:9093
- Couchbase exporter : http://localhost:9091/metrics
- Node Exporter      : http://localhost:9100/metrics
- collectd exporter  : http://localhost:9103/metrics
###  Destroy the prometheus stack
To destroy the stack run command `docker-compose down`

##  Installing and configuring grafana dashboards
Grafana is already deployed as container, hence we will be able to access the garafana portal on [localhost:3000](http:\\localhost:3000)

###  Login to grafana
Default credentails to access the grafana portal is as follows, you may configure the new password/ skip it.
- `username: admin`
- `password: admin`

###  Add data source
1. To add prometheus as data source to grafana, hoverover on gear icon  on left side of the portal and click on `datasource`
1. Click on `datasource` button on the right side of the page
1. Enter the URL of the prometheus as `http://prometheus:9090` and click `save & test`  at bottom of the page.

### Add dashboards to grafana
Grafana.com has pre-created dashboard which can be imported to our grafana portal.  
#### Import dashboards from grafana.com
1. Hover over `+` icon and select Import option on left side of the dashboard.
1. In import dashboard page, enter the dashboard ID (one at a time) and click on Load.
1. Click on Load to import the dashboard to our grafana portal
1. Select the datasource as newly created prometheus which you had configured.
1. Repeat the same steps for other dashboard IDs for below listed IDs.
    - Node exporter - 1860
    - Docker - 893, 395