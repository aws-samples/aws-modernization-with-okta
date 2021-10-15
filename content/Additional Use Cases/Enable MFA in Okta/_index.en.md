+++
title = "Enable MFA in Okta"
chapter = false
weight = 81
+++
In this use case, you will enable MFA with Okta Verify for every login to Okta and therefore to AWS SSO.

### Why introduce MFA?
Identity is the new perimeter and organizations introduce MFA to better protect access to application and services.

### Why Okta?
Just having a MFA solution is not enough, Organizations must be able to integrate it in a secure way for all applications. Okta provides over 7000 SSO Integrations for Cloud and On-Premise Applications. Okta protects all those applications with MFA and if you don't find them on the {{% button href="https://www.okta.com/integrations/" %}}Okta Integration Network (OIN){{% /button %}}, Okta supports open standards and other integration methods.

Introduction a second factor adds frictions to the end user experience. With Okta's {{% button href="https://www.okta.com/products/adaptive-multi-factor-authentication/" %}}adaptive Multi-Factor Authentication{{% /button %}}, Organizations define based on risk and context the right balance of security and user experience.

Okta provides a {{% button href="https://www.okta.com/products/adaptive-multi-factor-authentication/" %}}wide variety of vendor neutral factors{{% /button %}}. Here are few:
- Okta Verify: Smartphone App for Android and iOS that supports user friendly Push Notification and OTP
- U2F, FIDO2 & WebAuth: e.g. biometric authentication with Apple TouchID, Windows Hello and YubiKey
- Google Authentication
- Magic Link and OTP via Email
- OTP via SMS
- Integration of existing hardware tokens, legacy MFA solutions and OATH-OTP
- Passwordless authentication, Certificates and more

### Configuration Steps

Open the Okta Admin Console and go to "Security" -> "Multifactor".
Select "Okta Verify", set it to "Active" and set at least "Enable Push Notification". Save the settings.
![Enable Multifactor Okta Verify](/images/700_enable_multifactor_okta_verify.png)

Who and when the MFA enrollment is allowed can be configured in the tab "Factor Enrollment". A default configuration is provided and fine for the workshop.

The next step is to enforce MFA at Okta login. Go to "Security" -> "Authentication" and switch to the tab "Sign On". A default policy is already provided for all users. Click on "Add Rule".

![Add SSO Rule](/images/701_add_sso_rule.png)

Enter the Rule Name "MFA for Everyone", select "Prompt for Factor", select "Every Time" and click on "Create Rule".

![Add MFA Rule](/images/702_add_mfa_rule.png)

That's it. Okta will prompt you on the next login to enroll your MFA (Okta Verify) and on the following logins you must use it.

![Setup Okta Verify](/images/703_setup_okta_verify.png)