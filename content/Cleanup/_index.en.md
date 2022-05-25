+++
title = "Cleanup"
chapter = true
weight = 90
+++
If you used this Workshop for learning purposes and not for production you should always delete the created resources after you’re through all the steps.
In the AWS account go to settings under the SSO service and click on “Delete AWS SSO configuration”. You need to confirm that you understand that everything SSO related (including pushed users and groups) will be deleted by selecting the boxes and writing “DELETE” in the textbox

![Delete SSO](/images/delete_sso.png)

Clean up in Okta for a Free Developer Account is not required because no additional expenses are generated. Nevertheless, it’s a security best practice to delete unused users and applications in Okta. To delete the AWS SSO Application, go in the Okta Admin Dashboard to "Application" -> "Applications" and Deactivate and Delete "AWS Single Sign-On". If you created additional users, go to "Directory" -> "People" and Deactive & Delete them.

![Deactivate AWS SSO Application](/images/500_Delete_AWS_SSO.png)

![Delete AWS SSO Application](/images/510_Delete_AWS_SSO.png)