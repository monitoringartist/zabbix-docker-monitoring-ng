[<img src="https://monitoringartist.github.io/managed-by-monitoringartist.png" alt="Managed by Monitoring Artist: DevOps / Docker / Kubernetes / AWS ECS / Zabbix / Zenoss / Terraform / Monitoring" align="right"/>](http://www.monitoringartist.com 'DevOps / Docker / Kubernetes / AWS ECS / Zabbix / Zenoss / Terraform / Monitoring')

# Early alpha: Zabbix Docker Monitoring NG

This is early alpha (read **Not ready for production!**) version of Next
Generation of [zabbix-docker-monitoring](https://github.com/monitoringartist/zabbix-docker-monitoring).
It utilises Docker stats API only. It's similar to `docker.stats` implementation in [zabbix-docker-monitoring](https://github.com/monitoringartist/zabbix-docker-monitoring).

![zabbix-docker-monitoring-ng](https://raw.githubusercontent.com/monitoringartist/zabbix-docker-monitoring-ng/master/doc/zabbix-docker-monitoring-ng.png)

Requirements:
- Zabbix 3.4+: dependent items and JSON preprocessing
- Docker API v1.19+: disabling of container stats stream
- [zabbix-docker-monitoring](https://github.com/monitoringartist/zabbix-docker-monitoring): *docker.discovery* key

Please also vote for [preprocessing of LLD rules - ZBXNEXT-4087](https://support.zabbix.com/browse/ZBXNEXT-4087).
That's a reason why [zabbix-docker-monitoring](https://github.com/monitoringartist/zabbix-docker-monitoring)
is still required

# Installation

- download binary

```bash
wget -O /usr/bin/zabbix-docker-monitoring-ng \
https://raw.githubusercontent.com/monitoringartist/zabbix-docker-monitoring-ng/master/bin/zabbix-docker-monitoring-ng
```

- create new `Userparameter` definition in the Zabbix agent config file

```
UserParameter=docker-ng[*],/usr/bin/zabbix-docker-monitoring-ng $1
```

- install [zabbix-docker-monitoring](https://github.com/monitoringartist/zabbix-docker-monitoring)

- restart Zabbix agent

- import template [Template App Docker NG - www.monitoringartist.com.xml](https://raw.githubusercontent.com/monitoringartist/zabbix-docker-monitoring-ng/master/Template%20App%20Docker%20NG%20-%20www.monitoringartist.com.xml)

- link `Template App Docker NG - www.monitoringartist.com` to your host

# Author

[Devops Monitoring Expert](http://www.jangaraj.com 'DevOps / Docker / Kubernetes / AWS ECS / Google GCP / Zabbix / Zenoss / Terraform / Monitoring'),
who loves monitoring systems and cutting/bleeding edge technologies: Docker,
Kubernetes, ECS, AWS, Google GCP, Terraform, Lambda, Zabbix, Grafana, Elasticsearch,
Kibana, Prometheus, Sysdig,...

Summary:
* 2000+ [GitHub](https://github.com/monitoringartist/) stars
* 10 000+ [Grafana dashboard](https://grafana.net/monitoringartist) downloads
* 1 000 000+ [Docker image](https://hub.docker.com/u/monitoringartist/) pulls

Professional devops / monitoring / consulting services:

[![Monitoring Artist](http://monitoringartist.com/img/github-monitoring-artist-logo.jpg)](http://www.monitoringartist.com 'DevOps / Docker / Kubernetes / AWS ECS / Google GCP / Zabbix / Zenoss / Terraform / Monitoring')
