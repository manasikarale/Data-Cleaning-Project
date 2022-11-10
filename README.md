# Data-Cleaning-Project
### Team members: Ayesha Kesharia, Manasi Karale
#### Dataset background
The candidate summary file includes a financial summary for any candidate for the House, Senate, or President who has registered with the FEC or is listed on an official state ballot. This data is accessible for the current election as well as previous ones dating back to the 2008 election. There are also special elections for the House and Senate.

In each filing, committees give an overview of their financial activity. The candidate summary file is created by combining these summaries over the course of the whole two-year period. A link to the dataset files can be found in the References section. Totals for a candidate's finances include their main campaign committee as well as any additional committees permitted to raise money on their behalf. The totals range from January 1 of the year prior to the election to the date of the committees' most recent report.

We took up the file for 2021-2022 year and cleaned the dataset. The same cleaning steps were then implemented for the other 7 previous year's files. 
We found this dataset as a really good technique of applying some of the concepts that we learnt in the data cleaning class. 

Below link contains a description of the columns that we cleaned and checked based on the data dictionary that we found on the website. There are 50 columns and 4475 rows in the dataset.

URL: https://www.fec.gov/campaign-finance-data/candidate-summary-file-description/

#### Cleaning Steps and Columns Cleaned

Given the inaccuracy of data, we intended on scrubbing the following items:

| Column Name | Cleaning Agenda | Concept Used from Class | Python Techniques |
|-------------|-----------------|------------------------|-------------------|
|Link_Image | Made sure that the link has correct Cand_Id in it and ensured that it had the correct prefix and suffix | Understanding Tidy Data in Spreadsheets & Data Documentation and Curation | Lambda function |
|Cand_Name | Split the candidate name as First Name and Last Name | Understanding Tidy Data in Spreadsheets | String Split function, Lambda function |
|Cand_Id | Performing quality check on the pattern of Cand_Id | Data Documentation and Curation | Data frame sorting, Lambda function |
|Cand_Office | Improving readability of data by handling abbreviation of data | Understanding Tidy Data in Spreadsheets | String, Replace function |
|Cand_Office_St | Whitelisting Candidate Office State to check if the state name mentioned is correct, if not then modify it to 'Unknown' | Data Documentation and Curation | Lambda Function |
|Cand_State | Whitelisting Candidate State to check if the state name mentioned is correct, if not then modify it to 'Unknown' | Data Documentation and Curation | Lambda Function |
|Cand_Party_Affiliation | Whitelisting Party Affiliation Names to check if the party name mentioned is correct, if not then modify it to 'UNK' (where UNK represents 'Unknown' as per data dictionary) | Data Documentation and Curation | Lambda Function |
|Cand_Zip | Ensuring the validity of zipcode and formatting the zipcodes for better understanding | Data Documentation and Curtion | Lambda function and string transformations |
| Cand_Street_1 | Checking the format of street address and also modifying the invalid street address with blank values | Data documentation and Curation | Lambda function and string transformations |

#### Tools Used for Implementing the project
Python, Excel

Python libraries used: pandas, numpy, string, regex, math

#### Challenges

#### Limitations and Future Scope

#### References
https://www.fec.gov/data/browse-data/?tab=candidates
