# Titanic solution
## Table of Contents
1. Import Data and necessary packages
2. Getting information about Data
3. Handling null data
- 3.1. Remove data that can not be filled
- 3.2. Transform deck description
- 3.3. First class passengers
- 3.4. Second class passengers
- 3.5. Third class passengers
4. Handling categorical data
- 4.1 Change data types to numerical
- 4.2 One-hot encoding
5. Preprocess the Data an fit Random Forest Classifier
6. Preprocess test Data and predict

## Import Data and necessary packages.

In this part on the notebook I've just import necessary packages.

## Getting information about Data.

Grab the information from the dataset to know:
* how many rows, columns on it;
* has the dataset null, categorical values.

## Handling null data.

This part consist of five subtopics:
- firstly, I drop the rows with null value that can not be filled;
- secondly, cut the description of deck to feel later on null values in the Cabin column;
- then handling the null vlues in Cabin column to the each passenger class.
### Remove data that can not be filled.
I drop the rows which contain null values in columns Cabin and Fare.
### Transform deck description.
Сutting all the characters except the first one, allows me to quickly collect statistics on decks.
### First class passengers.
The distribution of first-class surviving passengers is the most implicit. Here, I simply determined the deck with the largest number of surviving passengers and filled in Cabin column.
### Second class passengers.
The distribution of surviving second-class passengers depends on the price of the ticket and, as a consequence, the deck. I set several conditions when filling in Cabin column.
### Third class passengers.
Similar to operations with second-class passengers.

## Handling categorical data.
