UPI Digital Payment Trend & Fraud Analysis
Project Overview

This project analyzes digital payment trends and detects possible fraud patterns in Unified Payments Interface (UPI) transactions using data analysis techniques.

The goal is to understand transaction behavior and identify suspicious activities using Exploratory Data Analysis (EDA), risk scoring, and visualization.

Objectives

Analyze digital payment trends.

Identify patterns in fraudulent transactions.

Build a risk scoring system to flag suspicious transactions.

Generate business insights from transaction data.

Dataset Features

The dataset includes the following columns:

transaction_id – Unique transaction ID

user_id – Unique user identifier

amount – Transaction amount

transaction_type – Payment type (Send / Receive)

device_type – Mobile device used

location – Transaction location

time – Transaction timestamp

is_fraud – Fraud label (0 = Legitimate, 1 = Fraud)

Tools & Technologies

Python

Visual Studio Code

Tableau

Python Libraries:

Pandas

NumPy

Matplotlib

Seaborn

Project Workflow
1. Data Cleaning

Handling missing values

Correcting data types

Removing duplicates

2. Exploratory Data Analysis (EDA)

Transaction distribution analysis

Fraud vs Non-fraud comparison

Time-based transaction patterns

3. Feature Engineering

Created new features such as:

Transaction hour

Risk score

Example:

df['risk_score'] = 0

df.loc[df['amount'] > 10000, 'risk_score'] += 2
df.loc[df['failed_attempts'] > 3, 'risk_score'] += 2

df['hour'] = pd.to_datetime(df['time']).dt.hour
df.loc[(df['hour'] >= 0) & (df['hour'] <= 5), 'risk_score'] += 1
Data Visualization

Key visualizations created:

Transaction amount distribution

Fraud transaction comparison

Hourly transaction trends

Failed attempt analysis

Dashboards can also be built using Tableau.

Key Insights

High-value transactions have a higher fraud risk.

Multiple failed attempts increase fraud probability.

Late-night transactions show unusual patterns.

Certain locations and devices show higher fraud frequency.

Business Recommendations

Implement real-time fraud monitoring systems.

Add extra authentication for high-value transactions.

Monitor late-night transactions more carefully.

Use machine learning models for automated fraud detection.

Future Improvements

Build fraud prediction models using machine learning.

Deploy a fraud detection system using Flask.

Create interactive dashboards using Power BI or Tableau.

Author

Pratiksha Bagwale Zagade

Aspiring Data Analyst focused on building real-world data analysis projects.