# SENRA PGR PDF Analysis

## Project Overview

This project analyzes a real-world dataset about seized, recovered, and arrested assets related to Angola's fight against corruption campaign by [PGR](https://www.pgr.ao/senra), from 2019 to 2024.

The data was extracted from a PDF published by [SENRA](https://www.senra.pgr.ao/) and compiled by [Pro Bono AO](https://probonoangola.org/).

*Focus*: This analysis focuses solely on asset values, categorized into five currencies (USD, AOA, AUD, CHF, and EUR) and converted to USD for consistency.

## Data Acquisition and Cleaning

While tools like pdfminer or PyPDF2 can be used for PDF extraction, Adobe Reader was chosen for this instance due to the presence of multiple currencies.

### Original Data

- 964 total assets

- Categorized as "seized," "recovered," or "arrested"

- Values in five currencies


### Cleaning Steps

- Converted all currencies to USD.

- Assigned a value of "0" to assets with "Aguarda Avaliação" (Awaiting Evaluation) status.

- Removed duplicate headers and inconsistencies.

- Transferred the cleaned data to a CSV file.

- Performed further cleaning with Python.

- Loaded the final data into a PostgreSQL database.

- Connected database to Power BI for visualization.


| **Original Name**   | **New Name**   |  **Description**                     |
|---------------------|----------------|--------------------------------------|
| .#                  |     asset      |  # of the asset                      |
| Bens                |      --        |  name of the asset                   |
| Valor               |     value      |  value of the asset                  |
| Orgao que recebeu   |    receiver    | institution that received the asset  |
| Situacao Actual     |     status     | status of the asset                  |
| Ano                 |      year      |  year the asset was processed        |


### Exploratory Data Analysis (EDA)

**Descriptive Statistics**

The project utilized Python to calculate statistics like mean, standard deviation, minimum, maximum, and frequency distributions for different data columns.



**Data Visualization** 

![Screenshot 2024-10-15 16 48 33](https://github.com/user-attachments/assets/c075a292-7363-4c8d-bfc8-5c00db6f8538)

![Screenshot 2024-10-15 17 54 35](https://github.com/user-attachments/assets/dee56613-1d58-427e-b21a-2e693ebacd71)

![Screenshot 2024-10-15 17 56 50](https://github.com/user-attachments/assets/d0f8280e-00d6-4fd2-9c9f-2dccc9ea83e7)

![Screenshot 2024-10-15 17 56 56](https://github.com/user-attachments/assets/80ef14d4-6bb2-4108-8a96-7da35835271e)




### Key Findings (Summary Table)

|Statistic	        |   Value  	    | Top Receiver	         |   Top Status	                             | Year |
|-------------------|---------------|------------------------|-------------------------------------------|------|
|Mean	              |  $59 Billion	| Cofre Geral da Justica | à guarda do fiel depositário (in custody) | 2021 |
|Standard Deviation |  $1 Trillion	|		                     |                                           |      |
|Minimum Value      |  $0			      |                        |                                           | 2019 |
|Maximum Value	    |  $23 Trillion	|		                     |                                           | 2024 |
|Arrested Assets    |  $24 Billion	|		                     |                                           |      |
|Seized Assets	    |  $23 Billion	|		                     |                                           |      |
|Recovered Assets   |  $3 Billion   |                        |                                           |      |




If you found this exploration of the data informative, and would like to see more in the future consider supporting my work! 

[Buying me a coffee](https://buymeacoffee.com/rickoalex) helps me dedicate time exploring new datasets and sharing valuable insights with the community.



### Tools and Technologies

- Adobe Acrobat Reader
- Microsoft Excel
- Power BI
- Python
- PostgreSQL



### Contributing:

Future improvements may involve automating the data extraction process with an ETL pipeline directly fetching data from the official website. 
Feel free to reach out with suggestions or improvements!





### License

<a href="https://opensource.org/license/mit">MIT License</a> 







Copyright (c) 2024 Ricardo Figueiredo
