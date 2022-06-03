+++
title = "Create Okta Groups"
chapter = true
weight = 30

+++
The assignment of Permissions Sets in AWS SSO can be configured per user. However, to be more flexible, we create and use groups.

We will create two groups in Okta for this workshop: “AWS PowerUserAccess” and “AWS ViewOnlyAccess”. The users will be managed in Okta and automatically provisioned to AWS SSO.

{{% notice info %}}
We will use groups that are managed in Okta, but as you can see in the screenshot are groups supported from multiple sources e.g. AD, LDAP, Workday, Google, and Microsoft365. On top of that, you can also create dynamic Groups in Okta e.g. based on User Attributes such as Department.
![Okta Group Sources](/images/40_okta_groups_sources.jpg)
{{% /notice %}}

{{% notice info %}}
Users in Okta can be provided from multiple sources. As you can see in the following screenshot are users supported from Workday, AD, ADFS as well as from multiple AD, multiple LDAP, Google and so on. This means that if a user is deactivated in AD, Okta will take care to deactivate the user in AWS SSO and other Apps (if supported by the App).
![Okta User Sources](/images/50_okta_user_sources.png)
{{% /notice %}}