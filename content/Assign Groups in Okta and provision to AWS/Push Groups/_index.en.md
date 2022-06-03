+++
title = "Push Groups"
chapter = false
weight = 52
+++
AWS SSO doesn’t know our groups yet. We will use the groups to map the Permission Sets in AWS SSO. Let’s push the groups and their memberships to AWS SSO.

Go to the tab “Push Groups” and click on “Find groups by name”. If you have more groups, you can also use “Find groups by rule”. But we keep it simple for this workshop.
![Start Push Groups Configuration](/images/240_start_push_groups_configuration.jpg)

Enter “aws” in the search field and select “AWS PowerUserAccess”.
![Push Groups aws PowerUserAccess](/images/250_push_group_aws_powerUserAccess.png)

{{% notice info %}}
If the group name exists not yet in AWS SSO, Okta will create a new one. Otherwise, an existing group will be linked.
{{% /notice %}}

Click on “Save & Add Another”. Repeat the same step for “AWS ViewOnlyAccess”.
![Push Groups Save and add another](/images/260_push_groups_save_and_add_another.png)

The configuration will look like this:
![Verify Push Grup Configuration](/images/270_verify_push_group_configuration.png)