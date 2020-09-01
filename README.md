# North Pacific Marine Salmon Diet Database

The North Pacific Marine Salmon Diet Database is a relational database for North Pacific salmon diet data, alongside relevant predator biological data (e.g., length, weight), prey biological data (e.g., caloric content, size), and environmental data (e.g., temperature, salinity). 

For users that are interested in the relational database, this repository includes a copy of the most up to data database (last update: 15 April 2020) built in MySQL along with all relevant documentation (directory: [npmsdd](https://github.com/mcarolinegraham/North_Pacific_Marine_Salmon_Diet_Database/tree/master/npmsdd)). While this database was specifically built to house salmon diet data, the core structure was designed in a manner that could be applied to other types of predator and prey data.

For users that are interested in the latest available data in the database but are not interested in working with the relational database format, this repository also contains csv files with available data (directory: [data](https://github.com/mcarolinegraham/North_Pacific_Marine_Salmon_Diet_Database/tree/master/data)), alongside preprocessing code to assist with further data analysis (directory: [code](https://github.com/mcarolinegraham/North_Pacific_Marine_Salmon_Diet_Database/tree/master/code)). The R code in this repository utilizes the csv files from the [data](https://github.com/mcarolinegraham/North_Pacific_Marine_Salmon_Diet_Database/tree/master/data) directory, but this same data can be found in the relational database format (`msdd_mysql_database_dump.zip`) in the [npmsdd](https://github.com/mcarolinegraham/North_Pacific_Marine_Salmon_Diet_Database/tree/master/npmsdd) directory.

## Getting started

To view and run the content in this repository, the user will need to download [R statistical software](https://www.r-project.org/), [R Studio](https://rstudio.com/products/rstudio/) and [MySQL](https://dev.mysql.com/downloads/) on their local machine.

## Repository Directories

### North Pacific Marine Salmon Diet Database (Directory: [npmsdd](https://github.com/mcarolinegraham/North_Pacific_Marine_Salmon_Diet_Database/tree/master/npmsdd))

* [npmsdd_data_entry_template](https://github.com/mcarolinegraham/North_Pacific_Marine_Salmon_Diet_Database/blob/master/npmsdd/npmsdd_data_entry_template.xlsx) - a blank xlsx template for NPMSDD data entry, there are 7 tabs that correspond to the 7 tables listed in the `npmsdd_documentation.pdf` under the subheading 'How to enter data using csv files'
* [npmsdd_mysql_database_dump](https://github.com/mcarolinegraham/North_Pacific_Marine_Salmon_Diet_Database/blob/master/npmsdd/npmsdd_mysql_database_dump.zip) - a dumped version of the MySQL database; contains up to date data and code to rebuild the database using MySQL
* [npmsdd_documentation](https://github.com/mcarolinegraham/North_Pacific_Marine_Salmon_Diet_Database/blob/master/npmsdd/npmsdd_documentation.pdf) - detailed information about the database design, database relations, database attributes, and data entry procedures

### Available Data (Directory: [data](https://github.com/mcarolinegraham/North_Pacific_Marine_Salmon_Diet_Database/tree/master/data))

* [data_descriptor](https://github.com/mcarolinegraham/North_Pacific_Marine_Salmon_Diet_Database/blob/master/data/data_descriptor.pdf) - detailed information about the data contained within each file of the [data](https://github.com/mcarolinegraham/North_Pacific_Marine_Salmon_Diet_Database/tree/master/data) directory; note that the columns contained in each of these csv files are also described in the `npmsdd_documentation.pdf` file however they have been rearranged to allow for easier data analysis in this version
* [diet_data](https://github.com/mcarolinegraham/North_Pacific_Marine_Salmon_Diet_Database/blob/master/data/diet_data.csv) - predator and prey data
* [predator_biological_data](https://github.com/mcarolinegraham/North_Pacific_Marine_Salmon_Diet_Database/blob/master/data/predator_biological_data.csv) - predator biological parameters data (e.g., length, weight) associated with diet data
* [prey_biological_data](https://github.com/mcarolinegraham/North_Pacific_Marine_Salmon_Diet_Database/blob/master/data/prey_biological_data.csv) - prey biological parameters data (e.g., caloric content, size) associated with diet data (`gear_type_prey_id == 1`) or potential prey items (`gear_type_prey_id != 1`)
* [environmental_data](https://github.com/mcarolinegraham/North_Pacific_Marine_Salmon_Diet_Database/blob/master/data/environmental_data.csv) - environmental data associated with diet data
* [sources](https://github.com/mcarolinegraham/North_Pacific_Marine_Salmon_Diet_Database/blob/master/data/sources.csv) - information about the sources from where the data were extracted
* [gear_type_predator](https://github.com/mcarolinegraham/North_Pacific_Marine_Salmon_Diet_Database/blob/master/data/gear_type_predator.csv) - information on gear type for predators
* [gear_type_prey](https://github.com/mcarolinegraham/North_Pacific_Marine_Salmon_Diet_Database/blob/master/data/gear_type_prey.csv) - information on gear type for prey

### R Scripts (Directory: [code](https://github.com/mcarolinegraham/North_Pacific_Marine_Salmon_Diet_Database/tree/master/code))

* [preprocessing_data](https://github.com/mcarolinegraham/North_Pacific_Marine_Salmon_Diet_Database/blob/master/code/preprocessing_data.Rmd) - uses the `diet_data.csv` file from the [data](https://github.com/mcarolinegraham/North_Pacific_Marine_Salmon_Diet_Database/tree/master/data) directory and provides code to help with preprocessing the diet data; it includes code to remove duplicate data, categorize salmon life stages, categorize time periods and to breakdown and edit the spatial data

## Authors

* Caroline Graham - database design and creation, code, drafting and revisions
* Dr. Brian Hunt - project concept, project funding, database design, review and revisions
* Dr. Evgeny Pakhomov - project concept, project funding, review and revisions

## Contributing

This repository is managed by the [Pelagic Ecosystems Laboratory](http://pelagicecosystems.oceans.ubc.ca/) within the Institute for the Oceans and Fisheries at the University of British Columbia. If you are interested in contributing data to the North Pacific Marine Salmon Diet Database, please contact Dr. Brian Hunt (b.hunt@oceans.ubc.ca).

## Data Usage

All data can be used under the license of CC BY with acknowledgement of authors.

## Version

Please note that this is version 1 of the North Pacific Marine Salmon Diet Database.

## Additional Notes

The authors acknowledge that this data may be eventually housed in another location and will update the information in this repository to reflect any changes to hosting. We used R version 3.6.1, RStudio version 1.2.1335, and MySQL version 8.0.18.

## Acknowledgements

We would like to acknowledge Raymond Ng for his guidance on the database design, and Marina Espinasse and Carmen Manuel for their assistance with data entry. We would also like to acknowledge Svetlana Naydenko, Alexey Khoruzhiy and Aleksey Somoff for helping to locate sources of data and Tim Spesivy and Kyoko Adachi for helping to translate Russian and Japanese sources.

## Funding

Funding for this project was provided by the Ambrose Monell and G. Unger Vetlesen Foundations, the University of British Columbia, and the Tula Foundation.