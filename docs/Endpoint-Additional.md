The `/additional` endpoint requires a single argument of claim number.
It returns miscellaneous data for the given claim.
```
/additional/<claim_num>.json
```
### Example
```
/additional/012345.json
```
### Fields
The following fields are returned for each row in the result set.
* claim_number
* other_claim_number
* claim_type
* denied_status
* loss_cause_code
* policy_number
* policy_begin_date 
* policy_end_date
* insured_address_1
* insured_address_2
* insured_city
* insured_state
* insured_zip_code
* insured_county
* insured_country
* deductible_amount
* loss_causation
