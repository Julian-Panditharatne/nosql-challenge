# NoSQL Challenge

This challenge consists of three main parts:

1. Setting up the Database and Jupyter Notebook.

2. Updating Database.

3. Exploratory Analysis.

## Part 1: Database and Jupyter Notebook Set Up

In this part of the challenge, I used MongoDB and PyMongo to do the following:

- Imported the data provided in the `establishments.json` file from the Terminal; naming the database **uk_food** and the collection **establishments**; and then copied the text that was used to import the data from the Terminal to a markdown cell near the start of the notebook.

- Created an instance of the Mongo Client within the `NoSQL_setup.ipynb`.

- Confirmed that importing the data from the Terminal had created the database, the collection, and loaded the data properly.

## Part 2: Update the Database

In this part of the challenge, I used PyMongo to do the following:

- Inserted the following information to the database:

```python
{
    "BusinessName":"Penang Flavours",
    "BusinessType":"Restaurant/Cafe/Canteen",
    "BusinessTypeID":"",
    "AddressLine1":"Penang Flavours",
    "AddressLine2":"146A Plumstead Rd",
    "AddressLine3":"London",
    "AddressLine4":"",
    "PostCode":"SE18 7DY",
    "Phone":"",
    "LocalAuthorityCode":"511",
    "LocalAuthorityName":"Greenwich",
    "LocalAuthorityWebSite":"http://www.royalgreenwich.gov.uk",
    "LocalAuthorityEmailAddress":"health@royalgreenwich.gov.uk",
    "scores":{
        "Hygiene":"",
        "Structural":"",
        "ConfidenceInManagement":""
    },
    "SchemeType":"FHRS",
    "geocode":{
        "longitude":"0.08384000",
        "latitude":"51.49014200"
    },
    "RightToReply":"",
    "Distance":4623.9723280747176,
    "NewRatingPending":True
}
```

- Found the BusinessTypeID for "Restaurant/Cafe/Canteen" and return only the BusinessTypeID and BusinessType fields.

- Updated the new restaurant with the found BusinessTypeID.

- Checked how many documents contained the Dover Local Authority; then removed any establishments within the Dover Local Authority from the database, and checked the number of documents to ensure they were deleted.

- Used *update_many* to convert number values that were stored as strings, and certain strings were replaced with None data type.

## Part 3: Exploratory Analysis

In this part of the challenge, I used pandas DataFrames and PyMongo to answer the following questions:

1. Which establishments have a hygiene score equal to 20?

2. Which establishments in London have a *RatingValue* greater than or equal to 4?

3. What are the top 5 establishments with a *RatingValue* of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?

4. How many establishments in each Local Authority area have a hygiene score of 0, sorted by highest number of establishments per Local Authority Area?

---

## **Repository Files and Folders**

Besides this `README.md` file, there are five other files, along with a folder containing one of the five files..

These are the four files that are not within the folder named **Resources**:

- `NoSQL_analysis.ipynb`: The Jupyter Notebook file containing the script used to perform the Exploratory Analysis portion of the challenge.

- `NoSQL_analysis_starter.ipynb`: The Jupyter Notebook file containing the starter code used in the `NoSQL_analysis.ipynb` script file.

- `NoSQL_setup.ipynb`: The Jupyter Notebook file containing the script used to perform the Database Setup and Update portions of the challenge.

- `NoSQL_setup_starter.ipynb`: The Jupyter Notebook file containing the starter code used in the `NoSQL_setup.ipynb` script file.

The **Resources** folder contains the following file:

- `establishments.json`: The JSON file containing the data to be imported into a MongoDB Database.

---

## **References**

MongoDB, Inc. (2024). *MongoDB documentation*. Mongodb.com. <https://www.mongodb.com/docs/>

*PyMongo 3.12.0 documentation — pymongo 3.12.0 documentation*. (2023, September 10). Pymongo.readthedocs.io. <https://pymongo.readthedocs.io/en/stable/index.html>
