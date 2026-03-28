# Grafana Observability Lab

This project shows a simple observability setup using Docker, Prometheus and Grafana. The goal is to understand how metrics are collected from an application and how they can be visualised in real time.

## Overview

The system is composed of three main components:

* A Flask application that generates metrics based on user requests
* Prometheus, which collects and stores these metrics
* Grafana, which displays the data through a dashboard

This setup simulates a basic DevOps observability pipeline where system behaviour can be monitored continuously.

## How to run the project

Before running the project, Docker Desktop must be installed and running.

Then, from the project folder, run:

```bash
docker compose up --build
```

## Access the services

Once the containers are running:

* Flask application → http://localhost:5000
* Prometheus → http://localhost:9090
* Grafana → http://localhost:3000


## What can be observed

The Flask application exposes a metric called `app_requests_total`, which increases every time the page is accessed. Prometheus collects this data and Grafana displays it as a time series graph.

By refreshing the application multiple times, it is possible to see how the metric changes in real time.

## Why this is relevant in DevOps

This lab shows how observability allows teams to understand system behaviour instead of only checking if a system is working or not. Having access to metrics helps identify patterns, detect anomalies and react faster to issues.

At the same time, the setup also shows that observability tools depend on correct configuration. Without proper integration between services, the data would not be visible, which highlights the importance of system understanding in DevOps environments.

## Reflection

During the setup, several issues appeared related to Docker configuration and service connectivity. These problems made it clear that observability is not only about using tools, but also about ensuring that the system is correctly configured.

The experience also showed that even a simple setup can represent the core idea of observability, while at the same time exposing the gap between a basic implementation and a production environment where security, scalability and monitoring strategies become more complex.

## Dashboard Example
<img width="955" height="514" alt="image" src="https://github.com/user-attachments/assets/3d284fec-1947-4049-a259-971e143441c9" />



## Technologies used

* Docker & Docker Compose
* Flask (Python)
* Prometheus
* Grafana

## Repository purpose

This repository was created as part of a DevOps laboratory to demonstrate practical observability concepts using real tools and a minimal working architecture.
