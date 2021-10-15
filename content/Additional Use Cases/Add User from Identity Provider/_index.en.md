+++
title = "Add User from Identity Provider"
chapter = false
weight = 85
+++

In this use case, we will discuss how to use Identity Provider as a user source. We will not do the full integration, but take a look at the capabilities and common use cases.

### Why use Identity Provider (IdP)?
Identity Provider are used to allow the login to Okta and therefore to AWS SSO with existing accounts of Google, ADFS, Facebook and so on.

### How is the sign-in experience with IdP?
The sign-in experience can be designed in multiple ways as you can see in the following screenshot:
- Routing Rules/ IdP Discovery: The user enters his username or email address and rules define the Identity Provider. You can see that the field to enter the password is not shown, because it makes no sense if the user is routed to an Identity Provider. Rules can be for instance a domain name e.g. all users with @partner.com will be redirect to a specific Identity Provider of a partner.
- Buttons: The user clicks on a button as shown in the screenshot to register or sign-in themself e.g. Smart Card, Facebook or Google.

![Login Widget IdP Buttons](/images/725_login_widget_IdP_buttons.png)

### Configuration Steps
Identity Providers are configured at "Security" -> "Identity Provider". Okta provides out of the box integration with multiple IdPs. {{% button href="https://developer.okta.com/docs/guides/add-an-external-idp/saml2/configure-idp-in-okta/" %}}Here are instructions on how to configure them{{% /button %}}

![Add Identity Provider](/images/720_add_identity_provider.png)

The next step is to create a routing rule. On the same page, switch to the tab "Routing Rules" and click on "Add Routing Rule" to create one.

![Add Routing Rule](/images/721_add_routing_rule.png)

Here is an example of such as routing rule. Every user which sign-ins with @gmail.com will be redirected to "My Google IdP".

![Configure Routing Rule](/images/722_configure_routing_rule.png)

After creating the rule you must activate it.
{{% notice warning %}}
Make sure that your admin user matches NOT the rule or you might lock out yourself.
{{% /notice %}}

![Activate Routing Rule](/images/723_activate_routing_rule.png)

After activating the routing rule, you can see the the field to enter the password is no longer shown.
![Username only login Widget](/images/724_username_only_login_widget.png)

To show the buttons of the Identity Providers (e.g. Sign in with Google), you have the following options:
- Custom URL domain: Go to "Settings" -> "Customization" and go through the wizard of "Custom URL Domain". This will allow you to configure the Okta Hosted Sign-In Widget to add the IdP at "Settings" -> "Customization" and go to the tab "Custom Sign In".
- Custom Okta hosted sign-in widget: Integrate the Okta Sign-In Widget at your own website as described {{% button href="https://developer.okta.com/code/javascript/okta_sign-in_widget/" %}}here{{% /button %}}.

![Custom URL Domain](/images/726_custom_URL_domain.png)