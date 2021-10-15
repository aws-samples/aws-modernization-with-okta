+++
title = "Value of adding Okta"
chapter = false
weight = 12
+++
When user access AWS Resources, organizations must make sure that the right people can access the right Resources in a secure way. Users can be employees, partners or customers. Their source of truth are HR Systems, AD or LDAP directories, Self Service Registration or Identity Providers.
Using the right source of truth is critical for Organzations to automate the Joiner-Mover-Leaver Process:
- Joiner: A new user joins the organization. Okta provides automated Birthright Access to AWS and other Applications to make them as productive as possible on their first day.
- Mover: As users change their job or role, get promoted, change their name due to marriage or go for leave of absence. Okta keeps the connected systems in sync and provides the right access.
- Leaver: At the end of the lifecycle, user leave immediately, time based, scheduled by the HR-System or by just deactivation them in an AD or LDAP directory. Okta deprovisions the access to keep the systems secure.

![Workforce Lifecycle Management](/images/1_Workforce_Lifecycle_Management.png)

Why Okta and AWS SSO?
- Setup SSO and Provisioning to AWS SSO with the pre-built Okta Integration Network app
- Automate joiner/mover/leaver scenarios with the advanced Lifecycle Management tools inside Okta
- Authenticate with AWS SSO using Okta as your Identity Provider using the new AWS CLI tools
- Add adaptive MFA based on context and risk and go password-less with Okta FastPass

![High Level Architecture](/images/2_High_Level_Architecture.png)

Okta together with AWS SSO provide flexible ways to control:
- Fine grained multi-account access management
- Attribute-based access control via Okta assertions or AWS SSO selection of synchronized Okta-user attributes
- Assign permission sets in AWS SSO or assign them as part of Okta user lifecycle management

![High Level Architecture2](/images/3_High_Level_Architecture2.png)

The AWS SSO integration is just one of many. {{% button href="https://www.okta.com/partners/aws" %}}Click here for all Okta Integrations with AWS.{{% /button %}}