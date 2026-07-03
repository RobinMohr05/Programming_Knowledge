aws cli can be installed in the company portal 


# log into your aws account 
```
aws sso login
```

## aws cli Setup
firstly you need to setup the aws config
```
aws configue sso
```

| aws option                                                             | what to enter                                                               |
| ---------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| aws session name                                                       | doesnt matter what it is - something along the lines of tecalliance-session |
| aws start url                                                          | https://ta-sso.awsapps.com/start/                                           |
| aws region                                                             | usually eu-central-1                                                        |
| sso registration scopes                                                | leave default (sso:account:access)                                          |
| window should open and access to your aws account is given to your CLI |                                                                             |
|                                                                        | choose the account you want to setup with in the CLI                        |
| default client region                                                  | eu-central-1                                                                |
| CLI-default output value                                               | skip or enter json                                                          |
| profile name                                                           | recommended to have one called default, doesn't matter afterwards           |
