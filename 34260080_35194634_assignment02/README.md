# FIT3182 Assignment 2 — AWAS Traffic Monitoring System

---

## Project Overview

A processing pipeline for an Automated Awareness Safety System (AWAS) that detects speed violations using static cameras. The pipeline uses Apache Kafka to produce event streams, Apache Spark Structured Streaming to join the different event streams and filter their contents for speed violations, and MongoDB for storing these violations according to a data retention policy.

### Python Dependencies

```bash
pip install pyspark==3.5.0 plotly
```

---

## Project Structure

```
34260080_35194634_assignment02/
├── README.md
├── src/
│   ├── 34260080_35194634_data_design_streaming.ipynb
│   └── 34260080_35194634_visualisation.ipynb
└── data/
    ├── vehicle.csv
    ├── camera.csv
    ├── camera_event_A.csv
    ├── camera_event_B.csv
    └── camera_event_C.csv

```

---

## How to Run

```bash
ipconfig
```

- copy the IPv4 address from the output in the terminal

```bash
docker run -v local_directory:container_directory -u user_group -p external_port_jupyter:internal_port_jupyter -p external_port_spark:internal_port_spark fit3182/pyspark jupyter notebook
```

```bash
docker run -d -p external_port_mongo:internal_port_mongo -v local_directory:container_directory fit3182/mongo
```

```bash
docker run -d -e KAFKA_ZOOKEEPER_CONNECT=IPv4_address:zookeper_port -e KAFKA_ADVERTISED_HOST_NAME=IPv4_address -p external_port_kafka:internal_port_kafka fit3182/kafka
```

```bash
docker run -d -p external_port_zookeeper:internal_port_zookeeper fit3182/zookeeper
```

```bash
pip install plotly pyspark==3.5.0
```

```bash
jupyter notebook --ip=0.0.0.0 --port=8888 --no-browser
```

---

## Generative AI Usage Declaration

Generative AI (Claude, Anthropic) was used to assist with:
- MongoDB schema design and index recommendations
- Plotly/Matplotlib visualisation code explanation and suggestion