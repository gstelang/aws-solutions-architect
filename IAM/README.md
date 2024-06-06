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

# Things to try
1. Login using sally user (dashboard -> sign in URL -> grab the username). You should be asked to change password.
2. Attach the s3_fulladmin.json policy to sally user
3. Remove #2. Attach the AllowAllS3ExceptCats policy
4. Test using catpics/ animalpics/
