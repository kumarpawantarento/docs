| #  | Field               | Description                                                          | Search Enabled | Filter Enabled | Mandatory | Type    | Source Type    |
| -- | ------------------- | -------------------------------------------------------------------- | -------------- | -------------- | --------- | ------- | -------------- |
| 1  | Id                  | Unique ID                                                            | FALSE          | FALSE          | Yes       | string  | auto generated |
| 2  | ref\_id             | Institute ID as per state records                                    | TRUE           | FALSE          | Yes       | string  | foreign key    |
| 3  | inst\_name          | Name of the institue                                                 | TRUE           | FALSE          | Yes       | string  | from state db  |
| 4  | education\_level    | The education level of the institute                                 | FALSE          | TRUE           | Yes       | string  | from state db  |
| 5  | students\_enrolled  | Number of students enrolled                                          | FALSE          | FALSE          | Yes       | string  | from state db  |
| 6  | teaching\_staff     | Number of teaching staff                                             | FALSE          | FALSE          | Yes       | string  | from state db  |
| 7  | nteaching\_staff    | Number of non-teaching staff                                         | FALSE          | FALSE          | Yes       | string  | from state db  |
| 8  | email               | Email address of the institute                                       | FALSE          | FALSE          |           |         |                |
| 9  | affiliation         | Whether institute is affiliated                                      | FALSE          | TRUE           | Yes       | boolean | from state db  |
| 10 | affiliation\_id     | ID if affiliated                                                     | FALSE          | FALSE          | No        | string  | foreign key    |
| 11 | course\_ids         | IDs of courses offered                                               | FALSE          | TRUE           | Yes       | array   | foreign key    |
| 12 | regulator           | Name of entity managing the institute                                | FALSE          | TRUE           | Yes       | string  | from state db  |
| 13 | inst\_medium        | Medium of instruction                                                | FALSE          | TRUE           | Yes       | string  | from state db  |
| 14 | start\_year         | Year in which institute was setup                                    | FALSE          | FALSE          | Yes       | string  | from state db  |
| 15 | instituteHead\_name | Name of head instructor of institute                                 | FALSE          | FALSE          | Yes       | string  | foreign key    |
| 16 | session\_id         | Academic calendar followed by the institute (summer/ winter closing) | FALSE          | FALSE          | No        | string  | foreign key    |
| 17 | location\_type      | Urban / rural                                                        | FALSE          | TRUE           | Yes       | string  | Masters        |
| 18 | district\_id        | District of the institute                                            | FALSE          | TRUE           | Yes       | string  | Masters        |
| 19 | block\_id           | Block of the institute                                               | FALSE          | TRUE           | Yes       | string  | Masters        |
| 20 | village\_id         | Village of the institute                                             | FALSE          | FALSE          | Yes       | string  | Masters        |
| 21 | constituency\_id    | Lok sabha constituency the institute is in                           | FALSE          | FALSE          | No        | string  | Masters        |
| 22 | pincode             | Pincode of the institute                                             | FALSE          | FALSE          | Yes       | string  | from state db  |
| 23 | gps                 | GPS location of the institute                                        | FALSE          | FALSE          | Yes       | latlong | from state db  |
| 24 | residence\_type     | Whether institute offers residential facility                        | FALSE          | FALSE          | No        | boolean | from state db  |
| 25 | url                 | URL of the institute's website, if any                               | FALSE          | FALSE          | No        | string  | from state db  |
| 26 | status              | Whether institute is active / closed                                 | FALSE          | TRUE           | Yes       | string  | from state db  |
