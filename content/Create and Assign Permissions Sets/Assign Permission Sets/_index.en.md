+++
title = "Assign Permission Sets"
chapter = false
weight = 62
pre = "<b>5.2 </b>"
+++

1. Go to **AWS accounts**, select an **AWS Account** and click on **Assign users or groups**.
![Select Accounts](/images/350_select_accounts.png)

2. Switch to Tab **Groups**, select **AWS PowerUserAccess** and click **Next**. The two displayed groups are the ones we provisioned from Okta to AWS IAM Identity Center.
![Assign group select group](/images/355_assign_group_select_group.png)

3. Click on **Next**.
4. Validate that you selected the group **AWS PowerUserAccess** and the permission set **PowerUserAccess**. Click on **Submit**.
![Complete assign group](/images/365_complete_assigned_group.png)

5. Repeat the same steps for **AWS ViewOnlyAccess** with the corresponding group and permission set.
6. Validate your configuration: You will have two Permission Sets which are assigned to the AWS Account via Groups.
![Validate AWS Account Configuration](/images/370_validate_aws_account_configuration.png)