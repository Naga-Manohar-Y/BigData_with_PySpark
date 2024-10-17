# arXiv metadata analytics with PySpark RDD and DataFrames
- Data source: https://www.kaggle.com/Cornell-University/arxiv/version/62

### Dataset Description

The ArXiv dataset, hosted on Kaggle, provides a rich collection of metadata from the extensive repository of scholarly articles available on ArXiv.org. This dataset includes approximately 1.7 million articles across a range of fields, including physics, computer science, mathematics, electrical engineering, biology, and economics. 

The dataset is particularly useful for machine learning applications due to its structure and comprehensive content. The metadata is provided in JSON format, with each entry containing key details such as:

- **ID**: Unique ArXiv identifier for each paper.
- **Submitter**: The individual who submitted the paper.
- **Authors**: List of authors for each paper.
- **Title**: Title of the paper.
- **Comments**: Additional details, such as page count and figure information.
- **Journal Reference**: Publication details if the paper has been published in a journal.
- **DOI**: Digital Object Identifier for locating the paper.
- **Abstract**: Summary of the paper.
- **Categories**: ArXiv categories/tags for the paper.
- **Versions**: History of versions available for the paper.

This dataset can support a range of analytics and machine learning applications, such as trend analysis, paper recommendation engines, co-citation networks, category prediction, and more. It’s updated weekly and available in a machine-readable format, making it ideal for use in text mining and data science projects.


## Anaytics with RDD

In this section, we are conducting an analytics case study on the ArXiv metadata dataset using PySpark's Resilient Distributed Datasets (RDDs). The dataset, which contains metadata for scholarly articles, is analyzed to gain insights into various attributes like titles, abstracts, and publication dates.

We perform the following tasks as part of this case study:
- **Data Loading and Initialization**: Load the ArXiv metadata JSON file into a PySpark RDD for distributed processing.
- **Data Exploration**:
  - Count the number of records and check the partitioning of the RDD.
  - Retrieve unique attributes, distinct licenses, and the shortest and longest article titles.
- **Text Processing**:
  - Extract abbreviations with five or more letters from article abstracts.
  - Calculate the number of articles published per month based on the 'update_date' attribute.
  - Compute the average number of pages in articles by analyzing the 'comments' field.
  
Through this project, we gain hands-on experience in working with PySpark RDDs, JSON data processing, and building custom functions to extract insights from unstructured text data. The project also demonstrates the use of Spark for scalable data processing, especially valuable for handling large datasets like ArXiv's metadata repository.


## Analytics with DF


In this section, we perform data analytics on the ArXiv metadata dataset using PySpark DataFrames. The dataset is loaded from a JSON file, enabling scalable and distributed data processing with Spark. Our objective is to explore various aspects of the data and derive meaningful insights through data transformation and querying.

#### Key Tasks:
- **Data Loading**: Load the ArXiv metadata JSON file into a Spark DataFrame and examine the data schema to understand the structure of the dataset.
- **Schema Redefinition**: Define a custom schema to streamline the data processing and bind it to the DataFrame for type consistency.
- **Missing Value Handling**:
  - Drop rows where the 'comments' attribute is null.
  - Replace null values in the 'license' attribute with 'unknown.'
- **SQL Queries**: Register the DataFrame as a temporary view for SQL-based querying to:
  - Identify authors who have published in the 'math' category.
  - List distinct licenses for abstracts containing five or more letters.
- **Statistical Analysis**:
  - Calculate statistics on the number of pages in articles with unknown licenses by extracting page numbers from the 'comments' field using a custom User-Defined Function (UDF).
  
Through this case study, we gain hands-on experience with PySpark DataFrames, JSON data ingestion, handling missing values, and running SQL queries on distributed data. The project demonstrates the power of Spark for processing large datasets and extracting valuable insights efficiently.