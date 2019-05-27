# sysmon

Monitor servers using Grafana, Influxdb,  telegraf

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

In order to run this project you have to install docker and docker-compose on your system.

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

6. Visit http://localhost:3000 to open grafana web view you can sign in using the following credentials:
```
username: admin
password: admin
```
7. on the left side menu hover over the plus `+` icon and press on `import`.

8. past the following url into text input with assosiated label `Grafana.com Dashboard`
https://grafana.com/dashboards/5955
and press load button.


## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/hassanjuniedi/sysmon/tags). 

## Authors

* **Hassan Juniedi** - *Initial work* - [Hassan Juniedi](https://github.com/hassanjuniedi)


## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
