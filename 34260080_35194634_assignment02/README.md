# FIT3182 Assignment 2 — AWAS Traffic Monitoring System

---

## Project Overview

An processing pipeline for an Automated Awareness Safety System (AWAS) that detects speed violations using static cameras. The pipeline uses Apache Kafka for to produce event streams, Apache Spark Structured Streaming to join the different streams and filter their contents for speed violations, and MongoDB for storing these violations according to a data retention policy.

## Prerequisites

|	Software			|	Version	|
|-----------------------|-----------|
|	Python				|	3.8+    |
|	Apache Kafka		|	3.x 	|
|	Apache Spark		|	3.5.x 	|
|	MongoDB				|	6.x+ 	|
|	Jupyter Notebook	|	Latest 	|

### Python Dependencies

```bash
pip install kafka-python pyspark pymongo pandas numpy matplotlib plotly
```

---

## Project Structure

```
34260080_35194634_assignment02/
├── README.md
├── src/
│   ├── 34260080_35194634_data_design_streaming.ipynb
│   ├── 34260080_35194634_producer_a.ipynb
│   ├── 34260080_35194634_producer_b.ipynb
│   ├── 34260080_35194634_producer_c.ipynb
│   └── 34260080_35194634_visualisation.ipynb
├── data/
│   ├── vehicle.csv
│   ├── camera.csv
│   ├── camera_event_A.csv
│   ├── camera_event_B.csv
│   ├── camera_event_C.csv
└── outputs/
```

---

## How to Run

```bash
```

---

## Generative AI Usage Declaration

Generative AI (Claude, Anthropic) was used to assist with:
- MongoDB schema design and index recommendations
- Plotly/Matplotlib visualisation code explanation and suggestion