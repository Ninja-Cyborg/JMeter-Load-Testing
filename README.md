# JMeter-Load-Testing
Performed Load Testing on [Reqres API](https://reqres.in/).  

# Key Learnings
# Requirements
# Environment Setup
# Test Execution
# Reports

# Key Learnings
- Executing Load Test: Performed over 7,000 requests ramped in 30 seconds
- Implemented Loop Controllers, Response Assertions
- Parametrisation for Authentication
- Both Happy Path and Bad Path requests were tested under load
- Generated Output Reports

# Requirements
- JMeter
- Java 8 or Higher

# Environment Setup
## Test Scripts:
- Basic api tests are generated in Browser using [BlazeMeter Chrome Extension](https://chrome.google.com/webstore/detail/blazemeter-the-continuous/mbopgmdnpcbohhpnfglgohlbhfongabi)

# Test Plan Structure
## User Defined Variables:
- api URL, Basic Auth Credntials

## Defining Loads/ Thread Groups
### CRUD Operations
- Most call will be made for CRUD operations, 250 Threads x 8 requests
- request performing CRUD operations on Users ad Resources
### Homepage requests
- Assumed that there will be less login and signup hits, 200 Threads x 4 
- includes basic request, login, register, open homepage
### Expection Paths
- bad requests will be least, 50 Threads x 5
- includes request leading to 400 or 404 error

# Test Execution
## JMeter UI
- [Download .jmx file](dummy-Rest-API-RECORD-01-22-23.jmx)
- Import the file in JMeter
- Before running *Disable Listerners*: Each Thread Group has Listerners, make sure to disable then while load testing. As the are resource hungry.
## Windows command line
- jmeter -n -t "specify location\filename" -l "location of .csv result reports" -e -o "location of html report folder"
## Linux 
- sh jmeter -n -t "specify location\filename" -l "location of .csv result report" -e -o "location of html report folder"

# Result Reports
- HTML Reports
- ![image](https://user-images.githubusercontent.com/66517017/233163834-92d1db4d-1f9a-40c7-ae4c-325ccceb1137.png)
- Logging Report
- [Logs](https://github.com/Ninja-Cyborg/JMeter-Load-Testing/blob/main/log_report.csv)
