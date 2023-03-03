+++
title = "Cleanup"
chapter = true
weight = 90
+++
If you used this Workshop for learning purposes and not for production you should always delete the created resources after you’re through all the steps.

1. In the AWS Management Console go to **Settings**, switch to the tab **Management** and click on **Delete**. You need to confirm that you understand that everything SSO related (including pushed users and groups) will be deleted.
![Delete SSO](/images/delete_sso.png)

2. Cleanup in Okta for a Free Developer Account is not required because no additional expenses are generated. Nevertheless, it’s a security best practice to delete unused users and applications in Okta. To delete the **AWS IAM Identity Center** Application, go in the **Okta Admin Dashboard** to **Application** -> **Applications** and click on **Deactivate**.
![Deactivate AWS IAM Identity Center Application](/images/500_Delete_AWS_SSO.png)

3. To delete it, click on **INACTIVE** and then **Delete**.
![Delete AWS IAM Identity Center Application](/images/510_Delete_AWS_SSO.png)

4. If you created additional users in Okta, go to **Directory** -> **People** and **Deactive & Delete** them.