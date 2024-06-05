# Specify parameters in parameters.json

```yaml
[
    {
      "ParameterKey": "sallypassword",
      "ParameterValue": "<strong-password"
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
