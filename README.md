PROJECT - 1

File Format Convertor

This script is a data conversion tool designed to convert CSV files to JSON format based on predefined schemas. 
It reads CSV files, applies a schema to structure the data, and then outputs the data in JSON format. 
The tool is configured to process multiple datasets defined in the provided schemas.json file.

Usage:-
1. Prerequisites:
•	Before using the tool, make sure you have the following:
•	Python installed (version 3.x)
•	Pandas library installed (pip install pandas)

1.	Configuration
Schemas File (schemas.json): Ensure that the schemas.json file is available in the source directory (SRC_BASE_DIR). This file contains the column details for each dataset.
2.	 Environment Variables:
Set the SRC_BASE_DIR environment variable to the source directory path.
Set the TGT_BASE_DIR environment variable to the target directory path where the JSON files will be stored.

Functionality:

  1.	get_the_columns_names:  Retrieves column names for a given dataset based on the provided schema.
  2.	read_csv:  Reads a CSV file, applies the schema, and returns a Pandas DataFrame.
  3.	to_json:  Converts a DataFrame to JSON format and saves the output to a specified file.
  4.	file_converter:  Converts all CSV files in a dataset to JSON format.
  5.	process_files:  Iterates over datasets and converts CSV files to JSON.

Notes:-

•	The script assumes that CSV files are located in the src_base_dir directory under individual dataset folders (e.g., src_base_dir/dataset1/part-01.csv).

•	The converted JSON files are stored in the tgt_base_dir directory under individual dataset folders.

•	If no CSV files are found for a dataset, a NameError is raised.

•	Any errors encountered during processing are caught, and the script continues with the next dataset.
