# 🎉 Thrilled to Share a Recent Azure Data Engineering Project! 🚀

In this project, I leveraged a variety of cutting-edge Azure tools and technologies to build a robust, scalable, and efficient data pipeline. The project follows the **Medallion Architecture** (Bronze, Silver, Gold) for data transformation and storage, ensuring that data is clean, well-structured, and ready for reporting and business decision-making.

Below is the detailed workflow and tools used:

## 🔹 **Data Ingestion:**
The first step was to ingest data from an **on-premises SQL Server** into **Azure Data Lake Gen2** using **Azure Data Factory** (ADF). The ingestion process was carried out dynamically via a **linked service** connected through **Self-Hosted Integration Runtime** (SHIR). This allows seamless integration of on-premises data with cloud services.

### Key Steps in Data Ingestion:
- **Source:** On-premises SQL Server.
- **Tool:** Azure Data Factory (ADF).
- **Method:** Dynamic ingestion via a linked service.
- **Runtime:** Self-Hosted Integration Runtime (SHIR).
- **Security:** Managed via **Azure Key Vault** for secure credential management.
- **Destination:** Data stored in **Azure Data Lake Gen2** under the **Bronze Layer**.
- The data was stored in its raw form, ready for transformation.

This architecture follows the **Medallion Architecture**, where the **Bronze Layer** serves as the landing zone for raw data.

## 🔹 **Data Transformation:**
Once the data was ingested into the **Bronze Layer**, the transformation process began using **Azure Databricks**. Databricks runs on top of **PySpark**, enabling efficient data processing and transformation at scale.

### Key Steps in Data Transformation:
- **Tool:** Azure Databricks with PySpark.
- **Process:** Data was pulled from the **Bronze Layer** in **Azure Data Lake Gen2**.
- **Transformation:** Data transformation was performed using **PySpark** in **Databricks notebooks**.
- **Connection:** Established via **Microsoft Entra ID** to securely access and process data in **Azure Data Lake**.
- **Result:** Transformed data was written into the **Silver Layer**, where it was cleansed, enriched, and prepared for further analysis.

### Transformation Process:
- Before beginning the transformation, the connection between **Azure Databricks** and **Azure Data Lake** was securely established using **Microsoft Entra ID**.
- The data transformation process was akin to refining crude oil into petrol, where raw data is cleaned, transformed, and enriched to add value.
- The transformed data was then stored in the **Silver Layer**, making it ready for analytics.

## 🔹 **Data Modeling with Synapse Analytics:**
To optimize query performance and enable seamless integration with external data sources, **Azure Synapse Analytics** was used to create **views** and **external tables**. 

### Key Steps in Data Modeling:
- **Tool:** Azure Synapse Analytics.
- **Task:** Creation of **views** for each table to provide a logical layer for accessing data.
- **External Tables:** **External tables** were built in Synapse, which allows querying data stored in **Azure Data Lake Gen2** without importing it into the Synapse SQL database, keeping the data in its original storage but accessible for analysis.

### Synapse Analytics Highlights:
- **Views:** Created for each transformed table to enable efficient querying.
- **External Tables:** Built on top of the metadata layer, enabling direct querying of data stored in **Azure Data Lake Gen2**.
- **Performance:** External tables provide optimized querying capabilities without the need for data duplication in Synapse SQL pools.

## 🔹 **Final Output in the Gold Layer:**
After the data was cleansed, enriched, and transformed, the final output was pushed into the **Gold Layer**. This layer contains the finalized data, which is now ready for reporting, business intelligence, and decision-making.

### Final Steps:
- **Tool:** Azure Data Lake Gen2 (Gold Layer).
- **Result:** The transformed data was stored in the **Gold Layer**, where it is ready for consumption by data analysts and business decision-makers.
- **Purpose:** Data in the Gold Layer is typically used for high-level reporting, dashboards, and business decision-making.

## 🛠 **Tools and Technologies Used:**
- **Azure Data Factory (ADF):** For dynamic data ingestion from on-premises SQL Server.
- **Azure Databricks:** For data transformation using PySpark notebooks.
- **Azure Synapse Analytics:** For data modeling, creating views and external tables.
- **Azure Data Lake Gen2:** For storing raw and transformed data in the Bronze, Silver, and Gold layers.
- **Microsoft Entra ID:** For secure access and authentication between services.
- **Azure Key Vault:** For managing credentials and ensuring secure access.

---

### **Key Takeaways:**
- This project provided hands-on experience with **Azure Data Factory**, **Azure Databricks**, **Azure Synapse Analytics**, and **Azure Data Lake Gen2**.
- I gained valuable knowledge in **data lake architecture**, **cloud security practices**, and **data transformation**.
- The Medallion Architecture (Bronze, Silver, Gold) provided a structured approach to managing and transforming data at scale.

---

This project helped me develop a deep understanding of **Azure Cloud** technologies and how they can be leveraged to build scalable, efficient data pipelines for real-world scenarios.

I am excited to continue exploring and working with Azure Data Engineering technologies and look forward to applying my skills in future projects and professional opportunities!
