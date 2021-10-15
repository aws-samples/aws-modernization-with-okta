+++
title = "Assign Users"
chapter = false
weight = 51
+++
To allow users access via SSO, we must assign them to the AWS SSO Application in Okta. As soon as you assign a user or group, Okta will call in the background the APIs to create the user in AWS SSO. If you change a mapped attribute e.g. FirstName, Okta will update the attribute also in AWS SSO. If you unassign a user, he will be deactivated in AWS SSO. Okta takes care of the full user life-cycle management.

Go to the tab “Assignment” and click on “Assign to Groups”.
![Assign to Groups](/images/210_assign_groups.jpg)

Click on “Assign” of both Groups. A dialog will appear to do additional attribute mapping per group. No changes are required, just confirm it. Finish the assignment by clicking “Done”.
![Assign AWS Groups](/images/220_assign_each_group.png)

The configuration will look like this:
![Configured Groups](/images/230_validate_assignment_configuration.jpg)