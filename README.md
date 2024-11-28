[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/jzfQvm5J)
# Project

## Group 7
- **LEE, JIMIN** (ID: 20729482, GitHub: jleecg)
- **SHIN, Yunju** (ID: 20723012, GitHub: yshinac)
- **KIM, Hyunju** (ID: 20792810, GitHub: hkimbd)

## Overview
This project focuses on collecting historical stock price data for S&P 500 companies using the Yahoo Finance API, processing it, and uploading it to a MySQL database hosted on an AWS RDS cloud platform. The collected data will later be utilized for machine learning analysis.

## Features
- **Data Collection**: The project fetches historical stock price data for S&P 500 companies over the past 7 days, automatically collecting data every 7 days based on Hong Kong Time (HKT).
- **Data Processing**: Data is cleaned and organized before being uploaded to the database.
- **Database Integration**: Data is uploaded in batches to a MySQL database.
- **Scheduler**: The data collection process is automated with a scheduler that runs every 7 days at 08:00 AM HKT.
- **Machine Learning**: The collected data will be used for machine learning analysis on stock price trends and patterns.

## Prerequisites
- Python 3.x
- Required Python libraries:
  - `apscheduler`
  - `pandas`
  - `yfinance`
  - `pytz`
  - `requests`
  - `beautifulsoup4`
  - `mysql-connector-python`

## Setup Instructions
1. **Clone the Repository**:
   ```bash
   git clone <repository-url>
   cd <repository-directory>
