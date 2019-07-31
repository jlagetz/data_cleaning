## Accountability data checks

Much of what is here is from [ProPublica's Guide to Bulletproofing Data](https://github.com/propublica/guides/blob/master/data-bulletproofing.md) and are standard practices at NICAR.  

1. How many records are in the database? Does it seem to be in the correct range?  
2. Check for duplicates in cases where true duplicates would be a problem. It is a problem in, say voter records. But it's possible that someone made multiple campaign contributions.  
3. Check ranges: Are numeric fields in ranges that make sense. Anything too high or
too low? (For example: In voter registration data are the dates of birth too recent or too long ago?)  Note the problems, we likely can't fix them.  
4. Is there anything blank or missing? Note the problems.  
5. Is there information in the wrong field?  
6. Check for consistency issues - particularly on city, state and ZIP.   There likly will be inconsistencies on names and companies, but we are not standardizing them at this point. If  you need to clean city or state, create a new city_clean or state_clean field.
7. Create a five-digit ZIP Code called ZIP5 if one does not exist.  
8. Create a YEAR field from the transaction date, registration date, hire data.  
9. For campaign donation data, make sure there is both a donor AND recipient.  

`Document everything you do and save scripts and syntax so that another person can check your work.`
