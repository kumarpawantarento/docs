| #  | Field            | Description                                      | Search Enabled | Filter Enabled | Mandatory | Type    | Source Type    |
| -- | ---------------- | ------------------------------------------------ | -------------- | -------------- | --------- | ------- | -------------- |
| 1  | Id               | Unique ID                                        | FALSE          | FALSE          | Yes       | string  | auto generated |
| 2  | ref\_id          | workplace ID as per state records                | TRUE           | FALSE          | Yes       | string  | foreign key    |
| 3  | wp\_name         | Name of the workplace                            | FALSE          | FALSE          | Yes       | string  | from state db  |
| 4  | wp\_type         | Type of workplace                                | FALSE          | TRUE           | Yes       | string  | from state db  |
| 5  | wp\_hq           | Whether the workplace is a headquarter or not    | FALSE          | TRUE           | Yes       | string  | from state db  |
| 6  | branch\_no       | Number of branches of the workplace              | FALSE          | FALSE          | Yes       | string  | from state db  |
| 7  | n\_employee      | Number of employees in workplace                 | FALSE          | FALSE          | Yes       | string  | from state db  |
| 8  | wp\_own          | Type of ownership of workplace (public, private) | FALSE          | TRUE           | Yes       | string  | from state db  |
| 9  | wp\_head         | Head of the workplace                            | FALSE          | FALSE          | Yes       | string  | from state db  |
| 10 | starting\_year   | Year in which workplace was setup                | FALSE          | FALSE          | Yes       | string  | from state db  |
| 11 | location\_type   | Urban / rural                                    | FALSE          | TRUE           | Yes       | string  | Masters        |
| 12 | district\_id     | District of the workplace                        | FALSE          | TRUE           | Yes       | string  | Masters        |
| 13 | block\_id        | Block of the workplace                           | FALSE          | TRUE           | Yes       | string  | Masters        |
| 14 | village\_id      | Village of the workplace                         | FALSE          | FALSE          | Yes       | string  | Masters        |
| 15 | phone            | Contact number for the workplace                 | FALSE          | FALSE          | No        | string  | from state db  |
| 16 | email            | Email ID of the workplace                        | FALSE          | FALSE          | No        | string  | from state db  |
| 17 | constituency\_id | Lok sabha constituency the workplace is in       | FALSE          | FALSE          | No        | string  | Masters        |
| 19 | pincode          | Pincode of the workplace                         | FALSE          | FALSE          | Yes       | string  | from state db  |
| 20 | gps              | GPS location of the workplace                    | FALSE          | FALSE          | Yes       | latlong | from state db  |
| 21 | status           | Whether workplace is active / closed             | FALSE          | FALSE          | Yes       | string  | from state db  |
| 22 | url              | URL of the workplace's website, if any           | FALSE          | FALSE          | No        | string  | from state db  |
| 23 | no\_employees    | Number of employees in workplace                 | FALSE          | FALSE          | Yes       | number  | from state db  |
