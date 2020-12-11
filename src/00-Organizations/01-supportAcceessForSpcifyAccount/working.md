# Support Access For Specify Account

## Target

## AWS Organizations

### Service Controll Policy

```
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "DenySupportAccess",
      "Effect": "Deny",
      "Action": [
        "support:*"
      ],
      "Resource": [
        "*"
      ],
      "Condition": {
        "StringNotLike": {
          "aws:PrincipalArn": [
            "arn:aws:iam::*:supportAccess"
          ]
        }
      }
    }
  ]
}
```
