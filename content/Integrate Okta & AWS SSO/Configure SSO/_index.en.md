+++
title = "Configure SSO"
chapter = false
weight = 42
+++
Select the tab “Sign On” and then on “View Setup Instructions”.
Follow the instructions. The values in the instructions are generated for your Okta Tenant.
For the part of the Metadata, you can open it on a new browser tab and download the metadata.xml file.

![Sign-On Configuration](/images/sign_on_configuration.jpg)

{{%attachments style="green" title="Example Setup Instructions" pattern=".*(pdf)"/%}}

{{% notice tip %}}
The linked document is an example file that was created for this workshop. These files are dynamically created for you, so make sure you use your own one and not this example file.
{{% /notice %}}

{{% notice warning %}}
AWS Organization is mandatory to activate AWS SSO. If you don't have one when you activate AWS SSO, you might be prompted to create an AWS Organization.
You can find more detailed information on how to configure AWS organization in the link below:
**[AWS: Creating and configuring an organization](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_tutorials_basic.html)**
{{% /notice %}}
