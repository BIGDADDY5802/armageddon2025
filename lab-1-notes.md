# Notes and Research

Source: 
<https://docs.aws.amazon.com/secretsmanager/latest/userguide/auth-and-access_resource-policies.html>

<https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_elements_principal.html#Principal_specifying>

```
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "ReadSpecificSecret",
      "Effect": "Allow",
      "Action": ["secretsmanager:GetSecretValue"],
      "Resource": "arn:aws:secretsmanager:<REGION>:<ACCOUNT_ID>:secret:lab/rds/mysql*"
    }
  ]
}
```
This policy allows the action `secretsmanager:GetSecretValue` on a specific secret in AWS Secrets Manager. The resource ARN specifies a secret located in a particular region and account, with a name that starts with `lab/rds/mysql`.

Database Security Group
![](/armageddon-db-sg.png)


Instance Security Group
![](/armageddon-instance-sg.png)