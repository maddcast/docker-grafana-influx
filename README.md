# Run containers
```
sudo docker-compose up -d
```
# Change grafana settings

- Open http://localhost:3000
- Enter admin/admin
- Change password
- Add datasource InfluxDB:
	- URL: http://influxdb1:8086
	- Database: telegraf
- Add dashboard panel
	- Datasource: InfluxDB
	- From: snmp
	- Select: field(uptime)
