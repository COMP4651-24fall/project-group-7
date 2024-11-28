[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/jzfQvm5J)
# Project

## Group 7
- **LEE, JIMIN** (Student ID: 20729482, ITSC: jleecg)
- **SHIN, Yunju** (Student ID: 20723012, ITSC: yshinac)
- **KIM, Hyunju** (Student ID: 20729810, ITSC: hkimbd)

## Overview
This project focuses on collecting historical stock price data for S&P 500 companies using the Yahoo Finance API, processing it, and uploading it to a MySQL database hosted on an AWS RDS cloud platform. The collected data will later be utilized for machine learning analysis.

## Features
- **Data Collection**: The project fetches historical stock price data for S&P 500 companies over the past 7 days, automatically collecting data every 7 days based on Hong Kong Time (HKT).
- **Data Processing**: Data is cleaned and organized before being uploaded to the database.
- **Database Integration**: Data is uploaded in batches to a MySQL database on AWS RDS.
- **Scheduler**: The data collection process is automated with a scheduler that runs every 7 days at 08:00 AM HKT.
- **Machine Learning**: The collected data will be used for machine learning analysis on stock price trends and patterns.

## Environment Setting in EC2 instance
- sudo apt install git
- sudo apt install python3 python3-pip
- pip3 install pandas numpy pymysql scikit-learn tensorflow

## Code Explanation
- **DailyDataCollectorToSQL.py** : Fetches historical stock price data for S&P 500 companies over the past 7 days, automatically collecting data every 7 days based on Hong Kong Time (HKT) using Scheduler.
- **master.py** : Distributes data into worker instances and get result from worekr instances
- **worker.py** : Get partition data from worker instance, train model with the data, and send the result to master instance
- **singeInstance.py** : Train the model with single instance

## Setup Instructions
1. **Clone the Repository**:
   ```bash
   git clone <repository-url>
   cd <repository-directory>
