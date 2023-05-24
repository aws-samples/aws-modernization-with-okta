+++
title = "Just-in-Time Access to AWS"
chapter = false
weight = 89
pre = "<b>7.8 </b>"
+++

Limiting human access to cloud resources is a key element of an effective security strategy. Although modern cloud architectures strive to eliminate the necessity for human access, there are still some scenarios where it is essential.

Configuration of this use case is out of scope for this workshop. [This AWS Blog post](https://aws.amazon.com/blogs/apn/just-in-time-least-privileged-access-to-aws-administrative-roles-with-okta-and-aws-identity-center/) describes how to use Okta Identity Governance (OIG) with AWS.

{{% notice info %}}
Okta Identity Governance (OIG) is not enabled in the free Okta Tenants. If you want to test it, please reach out to Okta to enable this feature in your Okta tenant.
{{% /notice %}}

Here is an example from the Blog-Post on how the access request flow is configured:
![Access Request Configuration](/images/770_access_request_configuration.png)