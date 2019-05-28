# sysmon
![version](https://img.shields.io/badge/version-1.0.2-blue.svg)
[![contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat)](https://github.com/hassanjuniedi/sysmon/issues)
[![HitCount](http://hits.dwyl.io/hassanjuniedi/sysmon.svg)](http://hits.dwyl.io/hassanjuniedi/sysmon)
[![Join the chat at https://gitter.im/sysmon-docker/community](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/sysmon-docker/community)
![size](https://img.shields.io/badge/size-200kB-green.svg)
![telegraf size](https://img.shields.io/badge/telegraf%20image-80MB-green.svg)
![influxdb size](https://img.shields.io/badge/influxdb%20image-137MB-green.svg)
![grafana size](https://img.shields.io/badge/grafana%20image-248MB-green.svg)

Monitor servers using Grafana, Influxdb,  telegraf

![preview](https://i.imgur.com/VEGnSJT.png)

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

In order to run this project you have to install docker and docker-compose on your system.

[Install Docker](https://docs.docker.com/install/)

[Install Docker Compose](https://docs.docker.com/compose/install/)
### Installing

1. Clone this repo to you machine:

```
git clone https://github.com/hassanjuniedi/sysmon.git

```

2. after cloning you will have a sysmon directory, cd into that directory:

```
cd sysmon
```

3. create new directory to hold data for grafana container:

```
mkdir grafana && sudo chown -R 472:472 grafana
```
4. Export a hostname variable (this will be used in grafana dashboard)

```
export HOSTNAME='youhostname'
```
5. Run docker-compose up command to run all the services :

```
sudo -E docker-compose up -d
```

6. Visit http://localhost:3030 to open grafana web view you can sign in using the following credentials:
```
username: admin
password: admin
```
7. on the left side menu hover over the `cog` icon and select `data sources` from the menu.

![datasources](https://i.imgur.com/voxgUTu.jpg)

8. select the `InfluxDB` from available options and enter the following:
```
URL: http://influxdb:8086
Database: telegraf
```
then click `save and test` button.

8. on the left side menu hover over the plus `+` icon and press on `import`.

9. past the following url into text input with assosiated label `Grafana.com Dashboard`
```
https://grafana.com/dashboards/5955
``` 
and press load button.

10. In the import view select the influxDB source and press `import` button.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/hassanjuniedi/sysmon/tags). 

## Authors

* **Hassan Juniedi** - *Initial work* - [Hassan Juniedi](https://github.com/hassanjuniedi)


## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
