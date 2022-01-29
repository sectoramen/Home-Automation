# Home Automation

This repo implements two services using Docker:

1. HomeAssistant for home automation

2. HomeBridge to add Apple HomeKit integration

The following assumptions are made ... because this is how I run it at home :-)

- The Server running HomeAssistant and HomeBridge has an IP address of 192.168.1.4 (Either static or through DHCP reservation)
- Your router is at 192.168.1.1
- You have installed docker and docker-compose on your system

You should modify the docker-compose.yaml and replace the following if your network has different IP addresses:

- Replace 192.168.1.1 with your router's LAN IP address
- Replace 192.168.1.4 with your server's IP address

## Pre-Requisites

Create the docker network for the two containers by running:

`docker network create my_net --subnet 172.20.1.0/24`

Create the directories where the HomeAssistant and HomeBridge configurations will reside

`mkdir HomeAssistant HomeBridge`

Run the two containers:

`docker-compose up -d`
