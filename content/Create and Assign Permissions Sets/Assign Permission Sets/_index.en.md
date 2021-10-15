+++
title = "Assign Permission Sets"
chapter = false
weight = 62
+++
Select "AWS accounts", select an AWS Account and click on "Assign users".

![Select Accounts](/images/select_accounts.png)

Switch to Tab "Groups", select "AWS ViewOnlyAccess" and click "Next". The two displayed groups are the ones we provisioned from Okta to AWS SSO.

![Assign group select group](/images/assign_group_select_group.png)

Select the "ViewOnlyAccess" Permission set that we created in the previous set and click on "Finish".
![Assign group select permission set](/images/assign_group_select_permission_set.png)

Wait a moment and click on "Proceed to AWS accounts".
![Complete assign group](/images/complete_assigned_group.png)

Repeat the same steps for "AWS PowerUserAccess" with the corresponding group and permission set.

Validate your configuration: You will have two Permission Sets which are assigned to the AWS Account via Groups.
![Validate AWS Account Configuration](/images/validate_aws_account_configuration.png)