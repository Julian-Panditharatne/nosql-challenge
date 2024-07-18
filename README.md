# NoSQL Challenge

This challenge consists of three main parts:

1. Setting up the Database and Jupyter Notebook.

2. Updating Database.

3. Exploratory Analysis.

## Part 1: Database and Jupyter Notebook Set Up

In this part of the challenge, I did the following:

- Imported the data provided in the `establishments.json` file from the Terminal; naming the database **uk_food** and the collection **establishments**; and then copied the text that was used to import the data from the Terminal to a markdown cell near the start of the notebook.

- Created an instance of the Mongo Client within the `NoSQL_setup.ipynb`.

- Confirmed that importing the data from the Terminal had created the database, the collection, and loaded the data properly.

## Part 2: Update the Database

In this part of the challenge, I did the following:

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

---

## **Repository Files and Folders**



---

## **References**

MongoDB, Inc. (2024). *MongoDB documentation*. Mongodb.com. <https://www.mongodb.com/docs/>

*PyMongo 3.12.0 documentation — pymongo 3.12.0 documentation*. (2023, September 10). Pymongo.readthedocs.io. <https://pymongo.readthedocs.io/en/stable/index.html>
