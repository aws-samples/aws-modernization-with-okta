+++
title = "Push Groups"
chapter = false
weight = 52
+++
AWS IAM Identity Center doesn’t know our groups yet. We will use the groups to map the **Permission Sets** in the AWS IAM Identity Center. Let’s push the groups and their memberships to AWS IAM Identity Center.

1. Go to the tab **Push Groups** and click on **Find groups by name**. If you have more groups, you can also use **Find groups by rule**. But we keep it simple for this workshop.
![Start Push Groups Configuration](/images/240_start_push_groups_configuration.jpg)

2. Enter **aws** in the search field and select **AWS PowerUserAccess**. (If the group name exists not yet in AWS IAM Identity Center, Okta will create a new one. Otherwise, an existing group will be linked.)
![Push Groups aws PowerUserAccess](/images/250_push_group_aws_powerUserAccess.png)

3. Make sure **Push group memberships immediately** is selected. Click on **Save & Add Another**.
![Push Groups Save and add another](/images/260_push_groups_save_and_add_another.png)

4. Repeat the same step for **AWS ViewOnlyAccess**.
5. The configuration will look like this. Make sure that the **Push Status** is set to **Active**.
![Verify Push Grup Configuration](/images/270_verify_push_group_configuration.png)