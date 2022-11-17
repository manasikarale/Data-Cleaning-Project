# Data-Cleaning-Project
### Team members: Ayesha Kesharia, Manasi Karale
#### Dataset background

<div style="text-align: justify">
The candidate summary file includes a financial summary for any candidate for the House, Senate, or President who has registered with the FEC or is listed on an official state ballot. This data is accessible for the current election as well as previous ones dating back to the 2008 election. There are also special elections for the House and Senate.

In each filing, committees give an overview of their financial activity. The candidate summary file is created by combining these summaries over the course of the whole two-year period. A link to the dataset files can be found in the References section. Totals for a candidate's finances include their main campaign committee as well as any additional committees permitted to raise money on their behalf. The totals range from January 1 of the year prior to the election to the date of the committees' most recent report.

We took up the file for 2021-2022 year and cleaned the dataset. The same cleaning steps were then implemented for the other 7 previous year's files. 
We found this dataset as a really good technique of applying some of the concepts that we learnt in the data cleaning class. 

Below link contains a description of the columns that we cleaned and checked based on the data dictionary that we found on the website. There are 50 columns and 4475 rows in the dataset.

URL: https://www.fec.gov/campaign-finance-data/candidate-summary-file-description/
</div>
  
#### Analysis
1. Party that has the minimum number of candidates for year 2022.
2. Party in the maximum debt.
3. Party with the least amount of loan.
4. Candidate affiliation with Senate, House or President.
5. Comparing a party's progress over past 12 years.

#### Motivation
<div style="text-align: justify">
Since it is election season, we thought of doing something with the election dataset. It is the fundamental right of every American to vote and elect the most suitable representative. For that, it is essential to have a summary of all the candidates and a summary of the work that they have done so far. This can help decide whom to vote for. Hence, we decided to clean the candidate summary dataset. We planned on starting by cleaning the latest dataset which can then be used for reference purposes. We will also be cleaning the remaining 6 files. We strived on making the data user-friendly, readable, and accurate. Our purpose was also to make all the files standard (following a particular pattern) so that it becomes easy for the users to access the files and follow the same standard of data entry process in future files.
</div>

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
|Cand_Street_1 | Checking the format of street address and also modifying the invalid street address with blank values | Data documentation and Curation | Lambda function and string transformations |
|Individual_Contribution | Checking the accuracy of the calculations | Data documentation and Curation | Lambda function, math function and if-else statement |
|Total_Contribution | Checking the accuracy of the calculations | Data documentation and Curation | Lambda function, math function and if-else statement |
|Total_Loan | Checking the accuracy of the calculations | Data documentation and Curation | Lambda function, math function and if-else statement |
|Total_Loan_Repayment | Checking the accuracy of the calculations | Data documentation and Curation | Lambda function, math function and if-else statement |
|Total_Contribution_Refund | Checking the accuracy of the calculations | Data documentation and Curation | Lambda function, math function and if-else statement |
|Net_Contribution | Checking the accuracy of the calculations | Data documentation and Curation | Lambda function, math function and if-else statement |

#### Tools Used for Implementing the project
Python, Excel

Python libraries used: pandas, numpy, string, regex, math

#### Results
Results can be found in the URL below.

https://github.com/manasikarale/Data-Cleaning-Project/blob/7a3bfbd3d58575f0cd43d51dbe697c209be0a95c/Cleaned%20Data%20Results.pdf

#### Challenges
<div style="text-align: justify">
While we were implementing the logic in Python, we faced multiple errors from format issues, to brainstorming the logic of cleaning particular columns. We took the help of multiple documentations from the Internet to resolve the issues. Before diving into the project, we also read 'Tidy Data' by Hadley Wickham to understand the thorough meaning of clean data. 
</div>

#### Limitations and Future Scope
<div style="text-align: justify">
For columns Cand_State and Cand_Office_St we used the already existing dictionary of values from the dataset. But we can also explore to check if there are any existing in-built libraries which we can use to get a complete list of all the states in the U.S. This would make the cleaning process for those columns thorough and robust. We can also think of automating the entire process, so as a new file gets generated at the source our cleaning steps would be implemented without any human intervention.
</div>  

#### References
https://www.fec.gov/data/browse-data/?tab=candidates

https://www.fec.gov/campaign-finance-data/candidate-summary-file-description/

https://pandas.pydata.org/docs/user_guide/index.html#user-guide

https://numpy.org/doc/stable/numpy-user.pdf

https://docs.python.org/3/library/string.html

https://docs.python.org/3/library/re.html
