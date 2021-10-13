# Network Security project

This project aims to show how a simple monitoring system can be implemented using:

- Prometheus to collect data from a metrics API provided by a server,
- Grafana to display the collected data of Prometheus using a template,
- an NGINX Container used as a dummy server from where the data is collected.

The entire system runs on Docker containers connected with each other using a Docker network specified in the ```docker-compose.yml``` file.
