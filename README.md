# 🔄 Azure Data Factory: Full Load Pipeline from MySQL to Azure SQL

## 📽️ [Watch the Demo](https://drive.google.com/file/d/1C3HnVeTbDEC7u0cJeV-VeeFv-WO3J45H/view?usp=sharing)

## 📌 Project Overview

This project demonstrates how to set up a **full-load ETL pipeline** using **Azure Data Factory (ADF)** to extract data from an on-premises **MySQL database** and load it into an **Azure SQL Database**. The pipeline performs a complete refresh of data on a scheduled basis, without using incremental logic.

The project includes:
- Connecting on-premises MySQL via **Self-hosted Integration Runtime**
- Creating ADF datasets and pipelines
- Transferring full table data to Azure SQL
- Setting up daily or custom scheduled triggers

---

## 📐 Architecture

```text
On-Prem MySQL → ADF (Self-hosted IR) → Azure SQL Database

🛠️ Technologies Used
Azure Data Factory

Self-hosted Integration Runtime

MySQL Database (source)

Azure SQL Database (destination)

Linked Services, Datasets, Pipelines, Triggers

📦 Pipeline Description
Copy Data Activity pulls all records from the source table (ipltab) in MySQL.

Uses a MySQL linked service via Self-hosted IR.

Writes to Azure SQL Database table using a sink dataset.

Configurable schedule using ADF triggers for automation.

🧰 Setup Instructions
1. Create Linked Services
MySQL (with Self-hosted IR)

Azure SQL Database

2. Create Datasets
Source: MySQL Table (e.g., ipltab)

Sink: Azure SQL Table

3. Create ADF Pipeline
Use Copy Data activity

Configure source and sink datasets

Test with Debug

4. Add Trigger (Optional)
Click Add Trigger > New/Edit

Set schedule (e.g., daily at 6 AM)

Publish All

🚀 How to Run
Open Azure Data Factory

Go to Author > Pipelines

Select the pipeline and click Debug

Monitor run under Monitor > Pipeline Runs

🌟 Future Enhancements
Add incremental loading logic using LastModifiedDate

Add logging and monitoring for audit trail

Add email alerts for success/failure

📹 Demo Link
Click here to watch the video walkthrough

🧑‍💻 Author
Vivek Sharma
