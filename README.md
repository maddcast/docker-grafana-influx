1. Run containers
docker-compose up -d
2. Change grafana settings
Open http://localhost:3000
Enter admin/admin
Change password
Add datasource InfluxDB:
	- URL: http://influxdb1:8086
	- Database: telegraf
Add dashboard panel
	- Datasource: InfluxDB
	- From: snmp
	- Select: field(uptime)
