# Muna-s-Portofolio
Analytics Portofolio

# CSV to Excel use Excel and Google Colab Conversion and Its Problem 
##1. Use Excel
   Open new Excel, Data, Get Data, From File, From Text or CSV, choose your data csv, import, adjust file origin, delimiter, and data type detection, then load.

##2. Use Google Colab
import pandas as pd

# Read file CSV
df = pd.read_csv('EksporBatik_2010_2021.csv')

# Save to Excel format
df.to_excel('EksporBatik_2010_2021.xlsx', index=False)

##Not all lines are converted correctly, what is problem?
because the number of commas (as delimiters) does not match the metadata in the data

how do you know? 
1. create a new column on the left side of the unconverted dataset to count the commas
note that in each line there are no commas other than those used as delimiters
Count the commas : =LEN(B2)-LEN(SUBSTITUTE(B2;",";""))
Copy, paste and drag until the data is in the last row

3. Match with the dataset that has been uploaded in Excel or Google Colab
4. To analyze whether this is really happening due to different comma counts, you can compare the correct comma count (according to metadata or colored green) with the load data
filter method: select country, filter text, does not contain ","
