+++
title = "Enable MFA in Okta"
chapter = false
weight = 81
+++
In this use case, you will enable MFA with Okta Verify for every login to Okta and therefore to AWS IAM Identity Center.

### Why introduce MFA?
Identity is the new perimeter and organizations introduce MFA to better protect access to applications and services.

### Why Okta?
Just having a MFA solution is not enough, Organizations must be able to integrate it in a secure way for all applications. Okta provides over 7500 SSO Integrations for Cloud and On-Premise Applications. Okta protects all those applications with MFA and if you don't find them on the {{% button href="https://www.okta.com/integrations/" %}}Okta Integration Network (OIN){{% /button %}}, Okta supports open standards and other integration methods.

Introduction a second factor adds friction to the end-user experience. With Okta's {{% button href="https://www.okta.com/products/adaptive-multi-factor-authentication/" %}}adaptive Multi-Factor Authentication{{% /button %}}, Organizations define based on risk and context the right balance of security and user experience.

![Adaptive MFA](/images/7_adaptive_mfa.png)

Okta provides a {{% button href="https://www.okta.com/products/adaptive-multi-factor-authentication/" %}}wide variety of vendor neutral factors{{% /button %}}. Here are a few:

- Okta Verify: Smartphone App for Android and iOS that supports user-friendly Push Notifications and OTP
- U2F, FIDO2 & WebAuth: e.g. biometric authentication with Apple TouchID, Windows Hello and YubiKey
- Google Authentication
- Magic Link and OTP via Email
- OTP via SMS
- Integration of existing hardware tokens, legacy MFA solutions and OATH-OTP
- Passwordless authentication, Certificates and more

### Configuration Steps: Add Okta Verify Authenticator

1. Open the Okta Admin Console, go to **Security** -> **Authenticator** and click on **Add Authenticator**.
![Add Authenticator](/images/740_add_authenticator.png)

2. Click **Add** of **Okta Verify**. Okta supports even more Authenticators than the ones shown here, but they are not available as part of the free trial.
If you have a MacBook with TouchID, WindowsHello or a FIDO-compatible key like a YubiKey, you can also enable **FIDO2 (WebAuthn)**.
![Authenticator](/images/741_authenticators.png)

3. Select in the configuration dialog of Okta Verify

- **Push notification (Android and iOS only)**: This will allow using a push notification next to an OTP with the Okta Verify App on iOS and Android.
- **Okta FastPass (All platforms)**: This will allow passwordless login with the Okta Verify App on Mac, Windows, iOS and Android.
- **Show the "Sign in with OktaFastpass" button**: This will allow passwordless login with Okta Verify without entering a username or password.

![Setup Okta Verify](/images/742_okta_verify_setup.png)

4. Who and when the MFA enrollment is allowed can be configured in the tab **Factor Enrollment**. A default configuration is provided and fine for the workshop.

### Configuration Steps: AWS IAM Identity Center Sign-On Policy

The next step is to enforce MFA for the AWS IAM Identity Center Application.

1. Go to **Applications** -> **Application** and select the **AWS IAM Identity Center** Application
2. Switch to the tab **Sign On**, scroll down and click on **View policy details**.
![AWS IAM Identity Center App Sign-On Policy](/images/743_aws_sso_sign_on_policy.png)

3. A **Default Policy** was automatically assigned to the AWS IAM Identity Center Application.
This policy is shared across multiple applications. For simplicity, we will enforce MFA for all Applications, but you can also create a dedicated Policy just for AWS IAM Identity Center.

4. Click on **Add rule**.
![Default Policy Add Rule](/images/744_default_policy_add_rule.png)

5. Enter the Rule name **MFA for Everyone**.
![App Sign-On Policy Name](/images/745_app_sign_on_rule_name.png)

6. Select **Possession factor**. Okta will automatically show all the authenticators that are enabled in your Okta tenant that have the factor type possession.
![App Sign-On Policy Then](/images/746_app_sign_on_rule_then.png)

7. To enforce MFA on every login, select **Every sign-in attempt** and click on **Save**.
![App Sign-On Policy Reauthentication](/images/747_app_sign_on_rule_reauthentication.png)

8. That's it. Okta will prompt you on the next login to enroll your MFA (Okta Verify) and on the following logins, you must use it.

### Test
1. Go to the End User Dashboard.
![Okta End User Dashboard](/images/280_open_end_user_dashboard.png)

2. Click on the **AWS IAM Identity Center** Application.
![Start AWS IAM Identity Center App](/images/290_start_aws_sso_app.png)

3. The first time you sign in, you will be prompted to enroll in your MFA (Okta Verify).
![Setup Okta Verify](/images/703_setup_okta_verify.png)