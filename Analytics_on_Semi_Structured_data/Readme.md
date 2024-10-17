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
## Analytics with DF