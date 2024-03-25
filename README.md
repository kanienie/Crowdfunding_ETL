# Crowdfunding_ETL

The Crowdfunding ETL Mini Project focuses on developing an Extract, Transform, Load (ETL) pipeline using Python and Pandas, aimed at streamlining the process of converting crowdfunding data into a structured format suitable for database storage and analysis. This comprehensive project encompasses several critical stages, starting from data extraction from Excel files, data transformation including cleaning and formatting, and finally, loading the transformed data into CSV files for database integration.

Key Components of the Project:

Data Extraction: The project begins with extracting crowdfunding data from crowdfunding.xlsx and contact information from contacts.xlsx, using Pandas to read the data into DataFrames.

Data Transformation:

Creation of Category and Subcategory DataFrames involves splitting the combined 'category & sub-category' column into distinct 'category' and 'subcategory' columns, assigning unique sequential identifiers to each category and subcategory, and exporting these to CSV files.

The Campaign DataFrame transformation includes renaming columns, converting data types for numerical values, adjusting date formats for 'launched_at' and 'deadline' columns, and aligning 'category_id' and 'subcategory_id' with those in the Category and Subcategory DataFrames.

For Contacts DataFrame, the project provides options to use either Python dictionary methods or regular expressions to parse and structure contact information, creating columns for 'contact_id', 'first_name', 'last_name', and 'email'.
Data Loading: The transformed data is then loaded into four CSV files: category.csv, subcategory.csv, campaign.csv, and contacts.csv.

Database Integration:

An Entity-Relationship Diagram (ERD) is sketched to visualize the database schema, illustrating the relationships between the tables based on the structured CSV files.

SQL table schema is created for each CSV file, detailing data types, primary keys, foreign keys, and other constraints, compiled into crowdfunding_db_schema.sql.

A PostgreSQL database, named crowdfunding_db, is set up to store the loaded data, with tables created as per the schema.
Data from the CSV files is imported into the corresponding tables in the PostgreSQL database, with verification steps through SELECT statements to ensure data integrity.

Execution Steps:

The ETL scripts for data extraction and transformation are run in a Python environment, generating the structured CSV files.
The PostgreSQL database is prepared, and the SQL schema script is executed to create the tables.
CSV files are imported into the database, and data verification is performed to confirm successful data loading.

Challenges and Considerations:

The project requires careful attention to data types and formats during the transformation process, ensuring compatibility with the database schema.

Handling null values and data inconsistencies are critical for maintaining data integrity.

The project emphasizes the importance of a systematic approach to ETL processes, showcasing the practical application of Python and Pandas in data preparation and database management.

Overall, the Crowdfunding ETL Mini Project serves as a practical exercise in developing and executing an ETL pipeline, highlighting the essential steps from data extraction and transformation to database integration, fostering skills in data handling, Python programming, and database management.
