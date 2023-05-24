+++
title = "Create Permission Sets"
chapter = false
weight = 61
pre = "<b>5.1 </b>"
+++

1. Go to AWS Management Console and open the **IAM Identity Center**.
![Create Permission Set](/images/go_to_aws_sso.png)

2. Go to **Permission sets** and click on **Create permission set**.
![Create Permission Set](/images/300_create_permission_set.png)

3. You can choose between predefined or custom permission sets. For this Workshop, we keep it simple. Select **Predefined permission set** and **PowerUserAccess**. Click on **Next**.
![Create Permission Type](/images/305_create_permission_type.png)

4. Click **Next** and on the last page on **Create**.
5. Repeat the same steps for **AWS ViewOnlyAccess** with the corresponding predefined permission set.
6. Validate your configuration: You will have two Permission Sets that are assigned to the corresponding groups from Okta.
![Validate Permission Sets](/images/310_validate_permission_sets.png)