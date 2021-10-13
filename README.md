# Network Security project

This project aims to show how a simple monitoring system can be implemented using:

- Prometheus to collect data from a metrics API provided by a server,
- Grafana to display the collected data of Prometheus using a template,
- an NGINX Container used as a dummy server from where the data is collected.

The entire system runs on Docker containers connected with each other using a Docker network specified in the ```docker-compose.yml``` file.

# How to start and test

Run

```
$ docker-compose up
```

then open your Browser and enter

```
http://localhost:3000/
```

to reach the Grafana container. Log in with the defaul credentials ```admin```/```admin```. Navigate to ```Configuration``` > ```Data Sources```, add a Prometheus data source, enter ```http://192.168.20.100:9090``` as URL and select ```Browser``` as Access type.

Afterwards, go to ```Create``` > ```Import``` and import a Dashboard by providing an ID which you can find on the Grafana website, e.g. ```1860```. Finally, you can go to the dashboard and monitor the NGINX container. One could run some command within the NGINX container, such us a git clone, to see how the network usage changes.

To remove the containers run 

```
$ docker-compose down
```
