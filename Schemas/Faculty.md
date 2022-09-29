| #  | Field             | Description                               | Search Enabled | Filter Enabled | Mandatory | Type   | Source Type    |
| -- | ----------------- | ----------------------------------------- | -------------- | -------------- | --------- | ------ | -------------- |
| 1  | Id                | Unique ID                                 | FALSE          | FALSE          | Yes       | string | auto generated |
| 2  | ref\_id           | Faculty id as per state records           | TRUE           | FALSE          | No        | string | foreign key    |
| 3  | name              | Name of the faculty                       | TRUE           | FALSE          | Yes       | string | from state db  |
| 4  | fname             | Name of the faculty's father              | FALSE          | FALSE          | No        | string | from state db  |
| 5  | mname             | Name of the faculty's mother              | FALSE          | FALSE          | No        | string | from state db  |
| 6  | age               | age of faculty                            | FALSE          | FALSE          | Yes       | string | from state db  |
| 7  | gender            | gender of faculty                         | FALSE          | TRUE           | Yes       | string | from state db  |
| 8  | mstatus           | marital status of faculty                 | FALSE          | FALSE          | Yes       | char   | from state db  |
| 9  | profQualification | Professional qualification of the faculty | FALSE          | TRUE           | Yes       | string | from state db  |
| 10 | mobile            | Contact number for the faculty            | FALSE          | FALSE          | No        | string | from state db  |
| 11 | email             | Email ID of the faculty                   | FALSE          | FALSE          | No        | string | from state db  |
| 12 | location\_type    | Urban / rural                             | FALSE          | FALSE          | Yes       | string | Masters        |
| 13 | district\_id      | District of residence                     | FALSE          | TRUE           | Yes       | string | Masters        |
| 14 | block\_id         | Block of residence                        | FALSE          | TRUE           | Yes       | string | Masters        |
| 15 | village\_id       | Village of residence                      | FALSE          | TRUE           | Yes       | string | Masters        |
| 16 | jdate             | Joining date of faculty                   | FALSE          | FALSE          | Yes       | string | from state db  |
| 17 | institute\_id     | Institute the faculty is associated with  | TRUE           | TRUE           | Yes       | string | from state db  |
| 18 | course\_id        | Course faculty is associated with         | FALSE          | TRUE           | Yes       | array  | from state db  |
| 19 | workingstatus     | Working status of the faculty             | FALSE          | TRUE           | Yes       | string | from state db  |
| 20 | subject\_id       | Subject the faculty is associated with    | FALSE          | TRUE           | Yes       | array  | from state db  |
| 21 | rdate             | Retirement date                           | FALSE          | FALSE          | Yes       | string | from state db  |
| 22 | join\_date        | Date when faculty started working         | FALSE          | FALSE          | Yes       | string | from state db  |
