| #  | Field          | Description                            | Search Enabled | Filter Enabled | Mandatory | Type   | Source Type    |
| -- | -------------- | -------------------------------------- | -------------- | -------------- | --------- | ------ | -------------- |
| 1  | Id             | Unique ID                              | FALSE          | FALSE          | Yes       | string | auto generated |
| 2  | ref\_id        | Assessor id as per state records       | TRUE           | FALSE          | Yes       | string | foreign key    |
| 3  | name           | Name of the assessor                   | FALSE          | FALSE          | Yes       | string | from state db  |
| 4  | fname          | Name of the assessor's father          | FALSE          | FALSE          | No        | string | from state db  |
| 5  | mname          | Name of the assessor's mother          | FALSE          | FALSE          | No        | string | from state db  |
| 6  | age            | age of assessor                        | FALSE          | FALSE          | Yes       | string | from state db  |
| 7  | gender         | gender of assessor                     | FALSE          | FALSE          | Yes       | string | from state db  |
| 8  | assessor\_type | Institute assessor vs student examiner | FALSE          | TRUE           | Yes       | string | from state db  |
| 10 | assessor\_tag  | e.g., medical or non-medical assessor  | FALSE          | TRUE           | Yes       | string | from state db  |
| 11 | mobile         | Contact number for the assessor        | FALSE          | FALSE          | No        | string | from state db  |
| 12 | email          | Email ID of the assessor               | FALSE          | FALSE          | No        | string | from state db  |
| 13 | district\_id   | District of residence                  | FALSE          | TRUE           | Yes       | string | Masters        |
| 14 | block\_id      | Block of residence                     | FALSE          | TRUE           | Yes       | string | Masters        |
| 15 | village\_id    | Village of residence                   | FALSE          | FALSE          | Yes       | string | Masters        |
| 16 | workingstatus  | Working status of the assessor         | FALSE          | TRUE           | Yes       | string | from state db  |
