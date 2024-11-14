# Intermediate-Advanced-Power-BI-Bootcamp-Lab-1 : Data Import & Transformation
Skillsoft - Data Society 4-day Intermediate/Advanced Power BI Bootcamp.

***Below is the first lab exercise: Data Import & Transformation***

**1) Import Lab data files: Using import from file**

Import Lab files using the text/csv connector and the Folder connector for the files in the Country files folder you will need to use the folder connector (Fact table/ Look-up table) 

  ![image](https://github.com/user-attachments/assets/ed490475-fa9f-4bec-ae94-b7da2343a2d5)


Select combined and load to import all csv files from the folder into power query	 

(Note: This can be done only when the data headers are uniform and there are no junk rows on the top)

  ![image](https://github.com/user-attachments/assets/17bf9c73-4c5a-4de0-be9d-e212ac90a48c)

**Import the following csv files. (Dimension table/ Transaction table)**
a.Product-Category

b.Product Sub-Category

c.Product

d.Sale Region

e.Sales By Country Files

f.Salesperson

g.Power Cycle Sales Target	 

  ![image](https://github.com/user-attachments/assets/ef074b92-ec1b-4c0b-9824-01020d7c96d1)


Scan through all tables and ensure that the data fields are classified correctly. 

  ![Screenshot 2024-11-14 161722](https://github.com/user-attachments/assets/7abe7015-206f-47cd-8eb7-7a7330f163db)





Change date/time fields to Date only
Remove the Source name column as it is not a required column for any analysis 	



**2) Creating a Reseller Dimension table**

Create The Reseller table by selecting the Sales by Country table then right-click and select duplicate	 

  ![image](https://github.com/user-attachments/assets/7e2a56f5-7402-4be2-b9ed-e8c6fdcab6a1)


From the Home Tab select choose Columns and ensure that the following fields are selected from the list.

1.	Reseller Business Type
2.	Reseller
3.	Reseller CityState
4.	ResellerCountry	 

  ![image](https://github.com/user-attachments/assets/826d2ef8-03f9-4704-b2b2-1371a251c72c)


On you keyboard select Ctrl+A to select the entire table.
From the Home Tab select Remove Rows and Remove Duplicated	

  ![image](https://github.com/user-attachments/assets/c7acfdeb-0ff9-494a-b295-de584da0e724)


**3) Create a Reseller ID Index column**

From the Add Column tab select Index Column with the Index starting from 1
Right-click on the new Index column and Rename the Index Column to ResellerID

  ![image](https://github.com/user-attachments/assets/da297301-4978-4d36-a1ee-e5be9e885e7a)


	 
**4) Merging Tables**

From the Home tab select Merge Queries from the dropdown

  ![image](https://github.com/user-attachments/assets/55dbd902-ad5d-41ea-95c9-68ba1dc1f00b)


The Sales by Country table should already be selected at the top and for the table that you are merging from select the Reseller table from the dropdown list.

You will need to ensure that these table are connected by the Reseller name. Select the Reseller Column in both tables

  ![image](https://github.com/user-attachments/assets/bee09bae-d5f4-4322-b15b-093077ce4ebd)

  ![image](https://github.com/user-attachments/assets/34d489c0-2374-48d8-aaf8-a73ea2083496)

From the new Reseller.1 Column you will now be able to expand the table records by selecting the expansion arrows in the column
Select only the ResellerID and uncheck the “use original column name as prefix option”	 

  ![image](https://github.com/user-attachments/assets/d8c93917-de41-4548-9938-19d64664591a)


5) Column Splitting

Going back to the Reseller table you will need to split out the State name from the city so that they are separate columns, respectively.

![image](https://github.com/user-attachments/assets/776af64a-1cb3-482d-b870-a89b6460c9ca)

From the Home tab select Split Column option -> By Delimiter

![image](https://github.com/user-attachments/assets/70e98d36-1492-4918-8fc7-e3d6c72f5c10)

From the menu option you will need to ensure that the split at is set to each occurrence

![image](https://github.com/user-attachments/assets/49cf1168-8f60-4997-accc-38ba6058bb1e)

In the advanced options the number of columns to split should be set to 2 and the split into should be columns

Re-Name the columns as followed.

Reseller CityState.1 -> City 
Reseller CityState.2 -> State	 

![image](https://github.com/user-attachments/assets/ba2b65f8-69e9-4047-bead-5799fa841d5e)
