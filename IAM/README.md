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

```yaml
 aws cloudformation create-stack --stack-name demo-cfn --template-body file://</full-path> --parameters file://</full-path> --capabilities CAPABILITY_NAMED_IAM
{
    "StackId": "arn:aws:cloudformation:us-east-1:381491858622:stack/demo-cfn/348de3a0-2373-11ef-ad13-0afff321999b"
}
```