# 'Data' Directory

This directory includes data from the NPMSDD in csv format for users who are not interested in working with the data in the relational database format. It also includes a file (`data_descriptor.pdf`) which contains detailed information on the data contained in each csv file.

## Directory Contents

[data_descriptor](https://github.com/mcarolinegraham/North_Pacific_Marine_Salmon_Diet_Database/blob/master/data/data_descriptor.pdf) - detailed information about the data contained within each file of the [data](https://github.com/mcarolinegraham/North_Pacific_Marine_Salmon_Diet_Database/tree/master/data) directory; note that the columns contained in each of these csv files are also described in the `npmsdd_documentation.pdf` file from the [npmsdd](https://github.com/mcarolinegraham/North_Pacific_Marine_Salmon_Diet_Database/tree/master/npmsdd) directory however they have been rearranged to allow for easier data analysis in this version

[diet_data](https://github.com/mcarolinegraham/North_Pacific_Marine_Salmon_Diet_Database/blob/master/data/diet_data.csv) - predator and prey data

[predator_biological_data](https://github.com/mcarolinegraham/North_Pacific_Marine_Salmon_Diet_Database/blob/master/data/predator_biological_data.csv) - predator biological parameters data (e.g., length, weight) associated with diet data

[prey_biological_data](https://github.com/mcarolinegraham/North_Pacific_Marine_Salmon_Diet_Database/blob/master/data/prey_biological_data.csv) - prey biological parameters data (e.g., caloric content, size) associated with diet data (`gear_type_prey_id == 1`) or potential prey items (`gear_type_prey_id != 1`)

[environmental_data](https://github.com/mcarolinegraham/North_Pacific_Marine_Salmon_Diet_Database/blob/master/data/environmental_data.csv) - environmental data associated with diet data

[sources](https://github.com/mcarolinegraham/North_Pacific_Marine_Salmon_Diet_Database/blob/master/data/sources.csv) - information about the sources from where the data were extracted

[gear_type_predator](https://github.com/mcarolinegraham/North_Pacific_Marine_Salmon_Diet_Database/blob/master/data/gear_type_predator.csv) - information on gear type for predators

[gear_type_prey](https://github.com/mcarolinegraham/North_Pacific_Marine_Salmon_Diet_Database/blob/master/data/gear_type_prey.csv) - information on gear type for prey