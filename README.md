# JMeter-Load-Testing
Load Tests ran on public api


path:
- E:\Downloads\apache-jmeter-5.5\bin>jmeter -g "C:\Users\dell\Downloads\dummy-Rest-API-RECORD-01-22-23-9-42-08-PM (1).jmx" -l "C:\Users\dell\Downloads\dummy-api/report.csv" -e -o "C:\Users\dell\Downloads\dummy-api/html_report"    

# Requirements
# Environment Setup
# Test Execution
# Reports

# Requirements
- JMeter
- 

# Environment Setup
##  Test Scripts:
- Primary api tests are imported with [BlazeMeter Chrome Extension](https://chrome.google.com/webstore/detail/blazemeter-the-continuous/mbopgmdnpcbohhpnfglgohlbhfongabi) in .jmx format
- Test for looping through user ID's, resources and 

# Test Plan Structure
## User Defined Variables:
- api URL, Basic Auth Credntials
## Thread Groups:
##  Homepage Thread Group:
- Tests for Main page actions Login, Register, mislleneous 
## CRUD Operation Thread Group:
- Tests executing CRUD operations on User and Resources
## Exception Paths Thread Group
- Includes Request that lead to 400 or 404 error

## Listeners:
- View Results Tree
- Aggregated Reports

# Defining Loads
- Assumed that there will be less login and signup hits, 50 Threads x 8 (4 exception, 4 homepage group)
- Most call will be made for CRUD operations, 100 Threads x 8 requests 

# Test Execution
## JMeter UI
- Download the file
- Import and run the file in JMeter
## Windows command line
- jmeter -n -t "specify location\filename" -l "location of .csv result reports" -e -o "location of html reports"
## Linux 
- sh jmeter -n -t "specify location\filename" -l "location of .csv result report" -e -o "location of html reports"

# Reports
- HTML Reports
- CSV Report
