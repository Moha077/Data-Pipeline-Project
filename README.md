<div align="center">
  <div id="user-content-toc">
    <ul>
      <summary><h1 style="display: inline-block;">👨 Online Retail Data Pipeline 👷</h1></summary>
    </ul>
  </div>
  
  <p>Retail Data Pipeline with Terraform, Airflow, GCP BigQuery, dbt, Soda, and Looker</p>
    <a href="https://github.com/Moha077/Data-Pipeline-Project" target="_blank">Request Feature</a>
</div>
<br>

## 📝 Table of Contents

1. [ Project Overview ](#introduction)
2. [ Key Insights ](#features)
3. [ Project Architecture ](#arch)
4. [ Usage ](#usage)
5. [ Credits ](#refs)
6. [ Contact ](#contact)

<a name="introduction"></a>
## 🔬 Project Overview 

This project represents a comprehensive data engineering endeavor, during which I established an ELT data pipeline for the purpose of extracting, analyzing, and presenting insights derived from the dataset of a UK-based online retail company.

### 💾 Dataset

This is a transnational data set that contains all the transactions occurring between 01/12/2010 and 09/12/2011 for a UK-based and registered non-store online retail.

The dataset includes the following columns:

| **Column** | **Description** |
| :--------------- |:---------------| 
| **InvoiceNo** |  Invoice number. Nominal, a 6-digit integral number uniquely assigned to each transaction. If this code starts with the letter 'c', it indicates a cancellation.  |  
| **StockCode** | Product (item) code. Nominal, a 5-digit integral number uniquely assigned to each distinct product. |
| **Description**   |  Product (item) name. Nominal.  |
| **Quantity**   |  The quantities of each product (item) per transaction. Numeric.  |
| **InvoiceDate**   |  Invoice Date and time. Numeric, the day and time when each transaction was generated.  |
| **UnitPrice**   |  Unit price. Numeric, Product price per unit in sterling.  |
| **CustomerID**   |  Customer number. Nominal, a 5-digit integral number uniquely assigned to each customer.  |
| **Country**   |  Country name. Nominal, the name of the country where each customer resides.   |

### 🎯 Project Goals

- Set up the cloud infrastructure using Terraform.
- Set up your Airflow local environment with the Astro CLI and Docker.
- Create a data pipeline from scratch using Apache Airflow.
- Upload CSV files into Google Cloud Storage.
- Ingest data into BigQuery.
- Implement data quality checks in the pipeline using Soda.
- Integrate dbt and run data models with Airflow.
- Visualize insights using Looker Studio.

<a name="features"></a>
## 🕵️ Key Insights

- 💸 **Total Revenue by Country**
  - The UK 🇬🇧 is the country that generated the most of the company's revenue with over 7M followed by the Netherlands with 285k.
 
- 🎁 **Top 2 sold products**
  - **N°1:** "PAPER CRAFT, LITTLE BIRDIE" is the Top selling product with 24,5%
  - **N°2:** "MEDIUM CERAMIC TOP STORAGE JAR" is the second Top seller with 23%

 > These 2 products alone account for more than 40% of the sales.

- 📈 **Revenue by months**
  - The month with the most revenue is November with more than 1,1M.
  - The month with the lowest revenue is February.

> This can be explained by the months of October, November, and December having important holidays like Christmas, Halloween, etc... where people tend to give each other gifts.

<a name="arch"></a>
## 📝 Project Architecture

The complete data pipeline encompasses the subsequent stages :

- Setting up the infrastructure on GCP *(Terraform)*
- Downloading, processing, and uploading the initial dataset to a Data Lake *(GCP Storage Bucket)*
- Moving the data from the lake to a Data Warehouse *(GCP BigQuery)*
- Transforming the data in the Data Warehouse and preparing it for the dashboard *(dbt)*
- Checking the quality of the data in the Data Warehouse *(Soda)*
- Creating the dashboard *(Looker Studio)*
  
You can find the detailed information on the diagram below:
![Architecture](https://github.com/Moha077/Data-Pipeline-Project/assets/57560715/b75ff7c8-aa6d-4397-b860-a89d4b9b7592)

### 🌪️ Pipeline on Airflow
![pipline air](https://github.com/Moha077/Data-Pipeline-Project/assets/57560715/fddf6794-fa4e-413f-b623-5b71c0e4407d)

### ⚙️ Data Modeling
![model](https://github.com/Moha077/Data-Pipeline-Project/assets/57560715/20827783-4041-4d48-91c3-776ad9baf24e)

### 🛠️ Technologies Used

- **Infrastructure**: Terraform
- **Google Cloud Platform (GCP)**
  - Data Lake (DL): Cloud Storage
  - Data Warehouse (DWH): BigQuery
- **Astro SDK** for Airflow
- **Workflow orchestration:** Apache Airflow
- **Transforming data:** dbt (Data Build Tool)
- **Data quality checks:** Soda
- **Containerization:** Docker
- **Data Visualization:** Looker Studio

<a name="usage"></a>
## 💻 Usage

  
#### 1. Google Cloud Platform
Set up GCP

#### 2. Terraform
We use Terraform to build and manage GCP infrastructure. Terraform configuration files are located in the separate folder. There are 3 configuration files:

- terraform-version - contains information about the installed version of Terraform;
- variables.tf - contains variables to make your configuration more dynamic and flexible;
- main.tf - is a key configuration file consisting of several sections.

#### 3. Airflow

Start Airflow on your local machine .
Access the Airflow UI for your local Airflow project. To do so, go to http://localhost:8080/ and log in with 'admin' for both your Username and Password.
You should also be able to access your Postgres Database at 'localhost:5432/postgres'.
Run the pipeline and monitor its execution.

<a name="refs"></a>
## 📋 Credits

- This Project is inspired by the recent video of the Data With Marc

<a name="contact"></a>
## 📨 Contact Me

[LinkedIn](https://www.linkedin.com/in/hamza-elbelghiti/) •
[Gmail](hamzaouimohamed8@gmail.com)


