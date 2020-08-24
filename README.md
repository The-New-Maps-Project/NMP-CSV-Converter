# The New Maps Project Generate CSV v1.0

Use the Google Geocoding API to get Latittude and Longitude data for any specified town



## How to Use: 
NOTE: must have your own google cloud API key.

1. Enter Your Google Cloud API key
2. If you wish, enter an interval between API calls. Default is 400ms. Look in your Google Cloud API console for the average latency of your Geocoding API (or the 95 Percentile). These are good numbers to base the interval off of. Do not set to zero or very low, can overload and cause program to skip some lines and run with errors
3. Enter the state name for a google search (Ex: "Virginia" and "VA" should both be fine"). This is done so Google Geocoding can find the right town location (Ex: Springfield,MA or Springfiled,IL?)
4. Enter data in the following table format: Each line: random value (tab) town name (tab) population.

#### Input Format Example: 

1	Boston	692,600  
2	Worcester	185,428  
3	Springfield	153,606  
4	Cambridge	118,927  
5	Lowell	110,997  
6	Brockton	95,708  

*This data is the exact format of Demographics by Cubit town data for each state*

5. Wait for CSV data to load and generate. The program will give you a time estimate (in secs) and how many lines have been generated so far (NOTE: The "copy" button does not preserve line breaks in the right places)

## Resources
This program is meant to be used with Demographics by Cubit's data on towns and population of each state on it's own website. It takes care of " TIE" marks and commas from numbers (Ex: 130,000. The comma here does not affect the output of the code). If two towns have a tie, they are simply returned separately (with the same population).

## Output: 
will show in the black box. Format: town name, population, latitude, longitude

#### Example Output:

Providence,179883,41.8239891,-71.4128343  
Cranston,81456,41.7798226,-71.4372796  
Warwick,81004,41.7001009,-71.4161671  
Pawtucket,72117,41.878711,-71.38255579999999  
East Providence,47618,41.8137116,-71.3700545  
Woonsocket,41751,42.00287609999999,-71.51478390000001  
