+++
title = "AWS CLI Access"
chapter = false
weight = 88
+++
In this use case, you will sign in to the AWS CLI with Okta via AWS SSO.

AWS CLI v2 supports direct integration with AWS Single Sign-On (SSO). You can now create CLI profiles that are linked to SSO accounts and roles. The CLI will automatically retrieve AWS credentials from SSO and refresh them on your behalf. There are new commands to help manage the CLI SSO profiles. This eliminates the need to copy and paste temporary AWS credentials from the AWS SSO console.

Execute in a terminal ***aws configure sso*** and follow the instructions.
- **SSO start URL**: Sign in to the AWS Dashboard and copy the URL.
- **SSO Region**: Sign in to your AWS Account and copy the Region of AWS SSO.

{{< highlight ssh >}}
$ aws configure sso
{{< / highlight >}}

The output will be
{{< highlight ssh >}}
$ aws configure sso
SSO start URL [None]: https://d-99xxxxxx75.awsapps.com/start
SSO Region [None]: eu-central-1

Attempting to automatically open the SSO authorization page in your default browser.
If the browser does not open or you wish to use a different device to authorize this request, open the following URL:

https://device.sso.eu-central-1.amazonaws.com/

Then enter the code:

RXPC-JNHZ
The only AWS account available to you is: 00xxxxxxxx56
Using the account ID  00xxxxxxxx56
{{< / highlight >}}

You will be prompted to login into your AWS SSO via Okta. If you enabled MFA, then you must also provide a 2nd Factor. Additionally, you will also be prompted by AWS SSO to allow access.

![AWS CLI Authorize Request](/images/aws_cli_authorize_request.png)

After a successful authentication, you will be prompted to select one of the roles we configure as part of the workshop. Select one of them to create a local profile.

{{< highlight ssh >}}
There are 2 roles available to you.
> PowerUserAccess
  ViewOnlyAccess

Using the role name "PowerUserAccess"
CLI default client Region [eu-central-1]:                                                             
CLI default output format [None]: json                                         
CLI profile name [PowerUserAccess-00xxxxxxxx56]:
{{< / highlight >}}

To test the profile, execute ***aws sts get-caller-identity --profile profilenameABC***

For example, in our case, we used the command:
{{< highlight ssh >}}
$ aws sts get-caller-identity --profile PowerUserAccess-00xxxxxxxx56
{{< / highlight >}}

The output will be
{{< highlight ssh >}}
$ aws sts get-caller-identity --profile PowerUserAccess-00xxxxxxxx56
{
    "UserId": "AROAXXXXXXXXXXXXXUN6N:name@domain.com",
    "Account": "00xxxxxxxx56",
    "Arn": "arn:aws:sts::00xxxxxxxx56:assumed-role/AWSReservedSSO_PowerUserAccess_7aXXXXXXXXXXXX17/name@domain.com"
}
{{< / highlight >}}

This use case is based on {{% button href="https://www.okta.com/blog/2020/05/how-okta-aws-sso-simplifies-admin-and-adds-cli-support/" %}}this{{% /button %}} and {{% button href="https://aws.amazon.com/blogs/developer/aws-cli-v2-now-supports-aws-single-sign-on/" %}}this{{% /button %}} blog post. Kudos to those authors!
