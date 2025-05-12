# Data
Internship

Day 1 Task: Data Cleaning and Preprocessing
Started with downloading the datasets from Kaggle. 
Datasets taken are: Medical Appointment No Shows and Sales Data.

In the Medical Appointment Dataset, the float format was first changed to prevent the PatientID from changing into exponential form. 
Turning the datatype to int resulted in negative numbers due to the limitation of the int value range.
Afterward, we checked for nulls and duplicates in the dataset (if any), but didn't find any in the current dataset. 
Then, the data type was changed for Scheduled Day and Appointment Day to DateTime to keep the format consistent for Dates.
Next, the column names were checked, and wrong spellings/letter cases were corrected. 
Everything seems consistent and clean in the end. 


For Sales Dataset, 
ISO-8859-1 Encoding type was given to resolve issues pandas had while reading the file initially. 
Started the process by checking for Null and Duplicate values. No duplicates found, but Null values were present for AddressLine2, State, PostalCode, and Territory columns. 
For AddressLine2, State, and Territory, null values were replaced with Not Available since dropping or filling with other data felt inconsistent based on thousands of values to be filled.
As for Postal Code, we took the Mode of all the values. When value is numerical, we can fill with mean, median, or mode.
The column headers looked fine with no spaces or inconsistent letter cases, and were left unchanged. PRICEEACH was slightly changed to PRICEEACH_IN$ for better understanding.
The phone column was left as an Object datatype due to different formats based on countries.
