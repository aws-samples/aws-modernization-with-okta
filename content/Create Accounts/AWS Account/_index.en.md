+++
title = "AWS Account"
chapter = false
weight = 22
+++
# Prepare Your Lab Account

For this Workshop you will need Administrator Access to an AWS Account that is not part of an AWS Organization and that is not yet configured for AWS IAM Identity Center.

- If you don’t already have an AWS account with Administrator access: create one now
{{% button href="https://aws.amazon.com/getting-started/" %}}Click me to open an AWS Account {{% /button %}}
- You can also find additional Guidance on how to Create an AWS Account 
{{% button href="https://aws.amazon.com/premiumsupport/knowledge-center/create-and-activate-aws-account/" %}}Click me for guidance {{% /button %}}

{{% notice tip %}}
- Once you have an AWS account, ensure you create an IAM user with the AdministratorAccess managed policy attached to it. You will use this account for the workshop. As a best practice, NEVER use the AWS root account when you are able to use an IAM user instead! 
{{% /notice %}}