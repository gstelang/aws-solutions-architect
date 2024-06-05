# Install

```
brew install helm
brew install hashicorp/tap/terraform
``` 
 
# AWS commands

1. Configure profile here: ~/.aws/config
```
[profile iamadmin-general]
region = us-east-1
[profile iamadmin-prod]
region = us-east-1
[default]
region = us-east-1
output = json
```
2. Configure credentials: ~/.aws/credentials 

```
[iamadmin-general]
aws_access_key_id = 
aws_secret_access_key = 
[iamadmin-prod]
aws_access_key_id = 
aws_secret_access_key = 
[default]
aws_access_key_id = 
aws_secret_access_key = 
```




