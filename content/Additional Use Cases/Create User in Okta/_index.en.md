+++
title = "Create User in Okta"
chapter = false
weight = 83
+++
In this use case, we will create a new user in Okta and provide access to AWS SSO.

### Why manage users directly in Okta?
Managing users directly in Okta solves the challenge when organizations want to provide access to AWS Ressources to partners, but don't want to create them in AD.

### Configuration Steps
To create a new user in Okta, go to "Directory" -> "People" and click on "Add person". 
![Add People](/images/730_add_people.png)

Enter the information about the user. To provide access to AWS, start entering the group name of "AWS ViewOnlyAccess" and select it. Select "Send user activation email now", this will activate the user in Okta and an Email to set the initial password is send to the user. Click on "Save".

![Send User Actication Email](/images/731_send_user_activation_email.png)

{{% notice info %}}
If you don't select "Send user activation email now", Okta creates the User in a Staged state and you must activate it manually.
Additional user attributes can be set in the Profile Tab of the user.
{{% /notice %}}

Click on the link in the activation email and set the password.

Logout with your current user or open a new incognito browser. Login with the new user as described in the chapter "Test" from Okta or AWS. You will be promted to enroll your MFA and because we only assigned one group, you will only have access to "ViewOnlyAccess". 

![AWS Dashboard new Okta user](/images/732_aws_dashboard.png)

To disable the user and remove access to AWS SSO, go to "Directory" -> "People" and click on the user name.
![Select User](/images/733_select_user.png)

Click on "More Action" and "Deactivate".
![Deactivate User](/images/734_deactivate_user.png)

{{% notice info %}}
Okta deactivates users in the first place, because deleting a user can have a big impact e.g. what happens with the personal files of the user in a cloud drive, that is integrated with Okta? Should the manager get access to the files, should the files be deleted? To automate the full user journey, Okta has a no-code [Workflow Engine](https://www.okta.com/platform/workflows/workflows-for-lifecycle-management/) to define fine granular actions.
{{% /notice %}}

{{% notice info %}}
If you want to delete the user, click on the button "Delete" in the user profile that is shown after deactivation.
{{% /notice %}}