To run this program on your local machine (vs code etc.), you can clone this repo and change .ipynb file to a .py file. 
You can run this file as is if you use a Jupyter notebook

**Assumptions**
* Data provided in json format
* Data has to be organized and output into csv files
* The csv interfaces do not have primary keys and foreign keys
* Only one type of contactType can exist i.e. either address or phone number


The first function converts a **json file** to a **pandas dataframe**, the particular json file run in this program produces the following output:
![dataframe image](/static/final_payload.jpg)



The second function is creating the **csv interfaces** from the **pandas dataframe**, the display here is of the subscriber csv interface that was created: 
![csv image](/static/subscriber_csv.jpg)



**relational_tables.jpg**
This repository also incldues a potential relational database model, with columns that would specify relations between tables 
Each table has a primary key 
Each table other than the subscriber table includes subscriber id as a foreign key 
Both the address and phoneNumber table also have contactInformation id as a foreign key as it is linked to subscriber contact information in the json file given
To accurately specify the current data I have also added a last updated column to the subscriber, address and phoneNumber tables 