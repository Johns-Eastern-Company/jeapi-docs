The `/reserves` endpoint requires at least one argument but takes up to three.
It returns a sum of reserve data based on the arguments provided; individual reserve
records will not be returned.
```
/reserves/<from_date>/<to_date>/<claim_num>.json
```
To leave a field "blank", enter values like below:
* from_date = false
* to_date = false
* claim_num = all
```
/reserves/false/false/all.json
```
However, you may run this example above and find the server responds with an error:
```
{"error": ["At least one keyword argument is required."]}
```
So you'll need to provide at least one non-default argument. See examples for more.
### Dates
All dates must be in format `YYYYMMDD`. Additionally, dates and times are in UTC format and are returned as [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) strings.
### Examples
Getting the current reserves for a claim.
```
/reserves/false/false/012345.json
```
Getting reserves up to a specific date.
```
/reserves/false/20190101/all.json
```
### Fields
The following fields are returned for each row in the result set.
* claim_number 
* party_name
* ptd_indemnity 
* ptd_medical 
* reserve_indemnity 
* reserve_medical  
* incurred_indemnity 
* incurred_medical 
* incurred_def_atty 
* ptd_recoveries
* ptd_loss 
* ptd_def_atty 
* ptd_expense 
* ptd_total 
* reserve_loss 
* reserve_def_atty 
* reserve_expense 
* reserve_total 
* incurred_expense 
* incurred_total
