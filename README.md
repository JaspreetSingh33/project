
# 🚗 Real-Time Dynamic Pricing System for Smart Parking




## 📝 Project Overview

This project implements a real-time dynamic pricing system for smart parking management using data streaming with Pathway and visualizations via Bokeh and Panel. It dynamically adjusts parking prices based on real-time data such as occupancy, traffic, queue length, and special events to maximize efficiency and revenue.

We simulate data streaming from historical records and plot real-time pricing graphs for each parking lot using Bokeh-powered interactive dashboards.

---------------
## Tech Stack

| Layer         | Tools / Libraries               |
| ------------- | ------------------------------- |
| Language      | Python 3                        |
| Stream Engine | [Pathway](https://pathway.com)  |
| Visualization | Bokeh, Panel                    |
| Data Format   | CSV                             |
| Platform      | Google Colab                    |


----------------------------------------------
## Architecture Diagram




## 🏗️ Architecture Diagram

The following diagram illustrates the real-time dynamic pricing system architecture :

[![Architecture Diagram](https://i.postimg.cc/qvbrf8j5/Screenshot-2025-07-09-124252.png)](https://postimg.cc/jD7mPJVH)

> 🔗 Click on the image to view it in full resolution.

-----------------------------------------------------------



## ⚙️ Architecture & Workflow Explanation

1. Data Ingestion
We read a CSV file (dataset.csv) simulating historical parking data.

Pathway reads it in streaming mode, processing records at fixed intervals (autocommit_duration_ms=500).

2. Real-Time Processing (Model 2)
A custom UDF (compute_dynamic_price) computes the parking price based on:

Occupancy rate

Queue length

Traffic conditions

Vehicle type

Special event flag

This price is continuously calculated and updated as new rows arrive.

3. Real-Time Visualization
We use Pathway's .plot() method to bind real-time data to a custom Bokeh chart.

Panel serves this plot as an interactive live dashboard.



-------