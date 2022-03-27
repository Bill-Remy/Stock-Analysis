**Stock Analysis - Refactoring Code to Improve Performance**

# Project Overview and Purpose

The purpose of ths project was to change the approach for analyzing stocks to determine if we could improve run time performance by refactoring our original code.

# Project Results

## Run Time Improvement Results

The performace of the refactored code was 14-15% better than the base code.  Comparative times for the base code and refactored code are shown below.
Rune time for the 2017 Analysis was 0.996 seconds.

<img src="Resources/Base run time 2017.png" alt="Resources/Base run time 2017.png" width="200">

The run time for the refactored 2017 Analysis was 0.852 seconds.

<img src="Resources/Refactored run time 2017.png" alt="Resources/Refactored run time 2017.png" width="200" align=center>

The difference of 0.144 seconds was 14.5% faster.  The results for 2018 were nearly identical in improved run time performance.
| Performance Run  | Run Time   |
|------------------|------------|
|2017 Base Run     | 0.996 secs |
|2017 Refactored   | 0.851 secs |
|2018 Base Run     | 1.007 secs |
|2018 Refactored   | 0.848 secs |

## Code Development Comparison

The base code used the approach of cycling through each ticker symbol in the array of stocks and then the entire file to calculate volume and return. This approach required the script to process the entire file twelve times, one for each ticker symbol printing the results at the end of each ticker symbol.

<img src="Resources/Base code flow.png" alt="Resources/Base code flow.png" width="300">

The refactored code changed two main aspects to the approach.  First, arrays were defined to store the results of volume, starting and ending prices for each ticker symbol.  Second the nesting of analysis was reversed to only read the file one row at a time and calculate values for each ticker.  Results for the arrays are printed to the output area only at the end of reading the file.

<img src="Resources/Refactored code.png" alt="Resources/Refactored code.png" width="250" height="400">


# Summary and Conclusions

The performance improvment was accomplished by reversing the order of processing and only reading the file one data to make calculations.  The base code read the file of 3,013 records twelve times whereas the refactored code only read the file once for each record.  This results in substantial reduction in calculations and less processor time.  Also, using loops to print and format the data in the refactored code was an improvment.  The speed difference was visibly observable when running the two scripts sequentially.  

While the roughly 15% performance improvement is not large in the absolute time savings for this application it would be significant if the entire U.S Stock Market was processed for a year.  Currently there are 3,812 stocks on the U.S. Markets.  If the refactored coding approach were used to analyze the entire market the savings in time would be aproxmiately fortyfive seconds which would be noticeable to most users.

