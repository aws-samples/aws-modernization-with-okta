+++
title = "Create Permission Sets"
chapter = false
weight = 61
+++
Go to AWS SSO.

![Create Permission Set](/images/go_to_aws_sso.png)

Select "Permission sets" and click on "Create permission set"
![Create Permission Set](/images/create_permission_set.png)

The Wizard provides multiple options. For this Workshop, we use an existing job function policy. There are multiple "common" job functions already configured, but you can always create a custom permission set with the AWS managed policies or even with your own policy document.

Select "Use an existing job function policy", select "ViewOnlyAccess" and click on "Next.

![Create Permission Type](/images/create_permission_type.png)

Click "Next" and on the last page on "Create".

![Create Permission Review](/images/create_permission_review.png)

Repeat the same steps for "AWS PowerUserAccess" with the corresponding job function policies. 

Validate your configuration: You will have two Permission Sets that are assigned to the corresponding groups from Okta.
![Validate Permission Sets](/images/validate_permission_sets.png)