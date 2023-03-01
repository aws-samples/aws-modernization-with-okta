+++
title = "Assign Users"
chapter = false
weight = 51
+++
To enable SSO for specific users or groups, we must assign them in Okta to the AWS IAM Identity Center Application. As soon as you assign a user or group, Okta will call in the background the APIs to create the user in AWS IAM Identity Center. If you change a mapped attribute e.g. FirstName, Okta will update the attribute also in AWS IAM Identity Center. If you unassign a user, he will be deactivated in AWS IAM Identity Center. Okta takes care of the full user life-cycle management.

1. Go to the tab **Assignments** and click on **Assign to Groups**.
![Assign to Groups](/images/210_assign_groups.jpg)

2. Click on **Assign** of both Groups. A dialog will appear to do additional attribute mapping per group. No changes are required, just confirm it. Finish the assignment by clicking **Done**.
![Assign AWS Groups](/images/220_assign_each_group.png)

3. The configuration will look like this:
![Configured Groups](/images/230_validate_assignment_configuration.jpg)