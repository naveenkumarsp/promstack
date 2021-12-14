# Installing and configuring grafana dashboards
Grafana is already deployed as container, hence we will be able to access the garafana portal on (localhost:3000)[http:\\localhost:3000]

# Login to grafana
Default credentails to access the grafana portal is as follows, you may configure the new password/ skip it.
- `username: admin`
- `password: admin`

# Add data source
1. To add prometheus as data source to grafana, hoverover on gear icon  on left side of the portal and click on `datasource`
1. Click on `datasource` button on the right side of the page
1. Enter the URL of the prometheus as `http://prometheus:9090` and click `save & test`  at bottom of the page.

# Add dashboards to grafana
Grafana.com has pre-created dashboard which can be imported to our grafana portal.  
## Import dashboards from grafana.com
1. Hover over `+` icon and select Import option on left side of the dashboard.
1. In import dashboard page, enter the dashboard ID (one at a time) and click on Load
1. Click on Load to import the dashboard to our grafana portal
1. Select the datasource as newly created prometheus which you had configured.

### Dashboard IDs
- Node exporter -1860
- Docker - 893, 395