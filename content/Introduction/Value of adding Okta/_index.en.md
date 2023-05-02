+++
title = "Value of adding Okta"
chapter = false
weight = 12
+++
When users access AWS Resources, organizations must make sure that the right people can access the right Resources in a secure way. Users can be employees, partners or customers. Their source of truth are HR Systems, AD or LDAP directories, Self Service Registration or Identity Providers.
Using the right source of truth is critical for Organizations to automate the Joiner-Mover-Leaver Process:

- **Joiner:** A new user joins the organization. Okta provides automated Birthright Access to AWS and other Applications to make them as productive as possible on their first day.
- **Mover:** As users change their job or role, get promoted, change their name due to marriage, or go on leave of absence. Okta keeps the connected systems in sync and provides the right access.
- **Leaver:** At the end of the lifecycle, users leave immediately, time-based, scheduled by the HR-System, or by just deactivation them in an AD or LDAP directory. Okta deprovisions the access to keep the systems secure.

![Workforce Lifecycle Management](/images/1_Workforce_Lifecycle_Management.png)

The next step is to provide secure and user-friendly access is adaptive MFA. Okta provides you full control of the access policies to AWS such as

- allow access only from corporate-managed devices
- enforce phishing-resistant MFA factors like FIDO2 on every login
- include risk signals to define access based on the context of the user, device, app, network, location, and external signals

![Adaptive MFA](/images/7_adaptive_mfa.png)

Why Okta and AWS IAM Identity Center?

- Setup SSO and Provisioning to AWS IAM Identity Center with a pre-built Okta Integration Network App
- Automate joiner/mover/leaver scenarios with the advanced Lifecycle Management tools from Okta
- Provide secure access to AWS CLI by using Okta as your Identity Provider
- Add adaptive MFA based on context and risk or go password-less with Okta FastPass

![High-Level Architecture](/images/2_High_Level_Architecture.png)

Okta together with AWS IAM Identity Center provides flexible ways to control:

- Fine-grained multi-account access management
- Attribute-based access control via Okta assertions or AWS IAM Identity Center selection of synchronized Okta-user attributes
- Assign permission sets in AWS IAM Identity Center or assign them as part of Okta user lifecycle management

![High-Level Architecture2](/images/3_High_Level_Architecture2.png)

{{% notice tip %}}
The AWS IAM Identity Center integration is just one of many. {{% button href="https://www.okta.com/partners/aws" %}}Click here for all Okta Integrations with AWS.{{% /button %}}
{{% /notice %}}