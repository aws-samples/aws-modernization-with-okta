+++
title = "Add User from AD"
chapter = false
weight = 84
+++
In this use case, we will discuss how to use AD or LDAP as a user source. We will not do the full integration, but take a look at the capabilities and common use cases.

Go to "Directory" -> "Directory Integration" and click on "Add Active Directory".

![Add AD](/images/710_add_active_directory.png)

The next page will show the high-level architecture of the integration.

![Integration](/images/713_integration_short.png)

The AD Domain Controller(s) are usually deployed behind a firewall. Okta is using a lightweight agent for the integration that provides a lot of benefits:

- The AD Agent has only an outbound connection to Okta via the encrypted HTTPS protocol. This means organizations don't have to open their firewalls.
- It's recommended to install the AD Agent on a Domain-joined server. It must not run on the Domain Controller.
- The configuration is done in the Web interface of Okta (Directory -> Directory Integrations). No access to the Windows Server is required after installation.
- Okta can import User and Groups from AD. The imported Groups and their membership are shown in "Directory" -> "Groups". If users exist already in Okta you can define patterns to match users automatically or use the Webinterface to resolve the conflict.
- Okta can create, update and deactivate users in AD as well as manage AD group membership.
- Okta supports custom attributes and you are in full control what attributes are read or written at "Directory" -> "Profile Editor". You can even use Okta's Expression Language to transform the attributes for more complex use cases.
- Okta supports multiple AD and LDAP. If users exist in multiple directories, you can define the priority at "Directory" -> "Profiles sources". You can even define the source per Attribute e.g. you can define a specific AD to be the source of the department of all users.
- Okta supports delegate authentication. This means the password is validated in the AD and not in Okta, such that user can sign in with the same password they know already.
- Okta provides self-service functionality for password reset and account unlock for AD users.
- Okta supports Just-In-Time (JIT) provisioning, such that not all users must be imported in the first place and the latest data is imported on login.
- Okta supports Agentless Desktop SSO. If users come from a domain-joined device, then they will be automatically signed in to Okta without entering their username and password. As the name implies, no additional agents are required on the device of the user.

The next steps of the AD Integration are out of scope for this workshop. It's intuitive and you can do it on your own with some common sense. For detailed instructions, please see the official documentation [here](https://help.okta.com/en/prod/Content/Topics/Directory/ad-agent-workflow.htm).