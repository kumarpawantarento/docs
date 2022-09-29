| #  | Field             | Description                                                 | Search Enabled | Filter Enabled | Mandatory | Type   | Source Type    |
| -- | ----------------- | ----------------------------------------------------------- | -------------- | -------------- | --------- | ------ | -------------- |
| 1  | Id                | Unique ID                                                   | FALSE          | FALSE          | Yes       | string | auto generated |
| 2  | ref\_id           | Candidate ID as per state records                           | TRUE           | FALSE          | No        | string | foreign key    |
| 3  | name              | Name of the candidate                                       | TRUE           | FALSE          | Yes       | string | from state db  |
| 4  | fname             | Name of the candidate's father                              | FALSE          | FALSE          | No        | string | from state db  |
| 5  | mname             | Name of the candidate's mother                              | FALSE          | FALSE          | No        | string | from state db  |
| 6  | gname             | Name of the candidate's guardian                            | FALSE          | FALSE          |           |        |                |
| 7  | age               | age of candidate                                            | FALSE          | FALSE          | Yes       | string | from state db  |
| 8  | gender            | gender of candidate                                         | FALSE          | FALSE          | Yes       | string | from state db  |
| 9  | mobile            | Contact number for the candidate                            | FALSE          | FALSE          | No        | string | from state db  |
| 10 | email             | Email ID of the candidate                                   | FALSE          | FALSE          | No        | string | from state db  |
| 11 | location\_type    | Urban / rural                                               | FALSE          | TRUE           | Yes       | string | Masters        |
| 12 | district\_id      | District of residence                                       | FALSE          | TRUE           | Yes       | string | Masters        |
| 13 | block\_id         | Block of residence                                          | FALSE          | TRUE           | Yes       | string | Masters        |
| 14 | village\_id       | Village of residence                                        | FALSE          | FALSE          | Yes       | string | Masters        |
| 15 | occupation\_id    | Whether candidate is a student or working as a professional | FALSE          | TRUE           | Yes       | string | foreign key    |
| 16 | function\_id      | The specific job role candiate is part of                   | FALSE          | TRUE           | Yes       | string | foreign key    |
| 17 | institute\_id     | Institute the candidate is associated with                  | FALSE          | TRUE           | No        | string | from state db  |
| 18 | course/ class\_id | Course candidate is associated with                         | FALSE          | TRUE           | No        | string | from state db  |
| 19 | workplace\_id     | workplace the candidate is associated with                  | FALSE          | TRUE           | No        | string | from state db  |
| 20 | status            | Status of candidate - active / inactive                     | FALSE          | TRUE           | Yes       | string | from state db  |
