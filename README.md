# SENRA PGR PDF Analysis

## Project Overview

This project analyzes a real-world dataset about seized, recovered, and arrested assets related to Angola's fight against corruption campaign by [PGR](https://www.pgr.ao/senra), from 2019 to 2024.

The data was extracted directly from the [SENRA website](https://www.senra.pgr.ao/).

*Focus*: This analysis focuses solely on asset values, categorized into five currencies (USD, AOA, AUD, CHF, and EUR) and converted to USD for consistency.

## Data Acquisition and Cleaning

The data was extracted using BeautifulSoup and a sample of the code can be seen under the name Webscrapping_sample.ipynb


### Original Data

- 508 seized assets
- 229 recovered assets
- 146 arrested assets
- Values in five currencies


### Cleaning Steps

- Converted all currencies to USD.

- Assigned a value of "0" to assets with "Aguarda Avaliação" (Awaiting Evaluation) status.

- Dropped "Bens" column
  
- Removed duplicate headers and inconsistencies.

- Removed accents and fixed values inconsistencies
  
- Transferred the cleaned data to a CSV file.

- Performed further cleaning with Python.

- Loaded the final data into a PostgreSQL database.

- Connected database to Power BI for visualization.


| **Original Name**   | **New Name**   |  **Description**                     |
|---------------------|----------------|--------------------------------------|
| .#                  |     activo     |  # of the asset                      |
| Bens                |   _dropped_    |  name of the asset                   |
| Valor               |     valor      |  value of the asset                  |
| Orgao que recebeu   |    receptor    | institution that received the asset  |
| Situacao Actual     |     status     | status of the asset                  |
| Ano                 |      ano       |  year the asset was processed        |


### Exploratory Data Analysis (EDA)

**Descriptive Statistics**

The project utilized Python to calculate statistics like mean, standard deviation, minimum, maximum, and frequency distributions for different data columns.



**Data Visualization** 

![Screenshot 2024-11-07 16 59 35](https://github.com/user-attachments/assets/70a967ef-6d43-446c-96f5-346e16b898ac)

Status/category
![Screenshot 2024-11-07 16 58 56](https://github.com/user-attachments/assets/c5b80f64-8427-4960-bab6-07a44092d475)

Receiver/category
![Screenshot 2024-11-07 16 59 19](https://github.com/user-attachments/assets/29f3cf47-1484-495a-a4a2-e70e67c887d6)


[Donwload the PDF report here](https://drive.google.com/file/d/16dPjCh4YoqFHE67aHk2JTipeYukb_f91/view?usp=sharing) (!!Portuguese)

**Contact me if you want a link to play around with the Power BI visual report**




### Key Findings (Summary Table)

|Statistic	        |   Value  	    | Top Receiver	         |   Top Status	                             | Year |
|-------------------|---------------|------------------------|-------------------------------------------|------|
|Mean	              |  $59.5 Million| Cofre Geral da Justica | à guarda do fiel depositário (in custody) | 2021 |
|Standard Deviation |  $1.1 Billion	|		                     |                                           |      |
|Minimum Value      |  $0			      |                        |                                           | 2019 |
|Maximum Value	    |  $31 Billion	|		                     |                                           | 2024 |


If you found this exploration of the data informative, and would like to see more in the future consider supporting my work! 

[Buying me a coffee](https://buymeacoffee.com/rickoalex) helps me dedicate time exploring new datasets and sharing valuable insights with the community.



### Tools and Technologies

- Microsoft Excel
- Power BI
- Python
- PostgreSQL



### Contributing:

~~Future improvements may involve automating the data extraction process with an ETL pipeline directly fetching data from the official website.~~

Feel free to reach out with suggestions or improvements!
 




### License

<a href="https://opensource.org/license/mit">MIT License</a> 







Copyright (c) 2024 Ricardo Figueiredo
