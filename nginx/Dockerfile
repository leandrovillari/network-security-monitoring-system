FROM nginx:latest
RUN apt-get update && apt-get install -y wget iproute2 iputils-ping
RUN wget -P /home/ https://github.com/prometheus/node_exporter/releases/download/v1.1.2/node_exporter-1.1.2.linux-amd64.tar.gz
RUN tar xvfz /home/node_exporter-1.1.2.linux-amd64.tar.gz -C /home/
WORKDIR /home/node_exporter-1.1.2.linux-amd64
CMD [ "./node_exporter" ]