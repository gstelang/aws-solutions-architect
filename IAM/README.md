# Specify parameters in parameters.json

```yaml
[
    {
      "ParameterKey": "sallypassword",
      "ParameterValue": "<strong-password>"
    }
]
```
# Command

1. Create stack
```yaml
 aws cloudformation create-stack --stack-name demo-cfn --template-body file://</full-path> --parameters file://</full-path> --capabilities CAPABILITY_NAMED_IAM
```

2. To debug/check events
```yaml
aws cloudformation describe-stack-events --stack-name demo-cfn
```

# Some screen grab...

<img width="954" alt="Screenshot 2024-06-06 at 1 27 31 AM" src="https://github.com/gstelang/aws-solutions-architect/assets/58006887/6fe3a936-e598-4618-bd84-29b8cb4e271c">

# Things to try on console
1. Login using sally user (dashboard -> sign in URL -> grab the username). You should be asked to change password.
2. Attach the s3_fulladmin.json policy to sally user (Attach it inline using json)
3. Remove #2. Attach the AllowAllS3ExceptCats policy (add permissions -> attach policies directly). You should see the policy like
```yaml
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Action": "s3:*",
            "Resource": "*",
            "Effect": "Allow"
        },
        {
            "Action": "s3:*",
            "Resource": [
                "arn:aws:s3:::demo-cfn-catpics-gzyvp0g3niwt",
                "arn:aws:s3:::demo-cfn-catpics-gzyvp0g3niwt/*"
            ],
            "Effect": "Deny"
        }
    ]
}
```
5. Test using catpics/ animalpics/

# clean up resources
1. Delete all the contents from the s3 bucket.
2. Delete stack
```yaml
aws cloudformation delete-stack --stack-name demo-cfn 
```