+++
title = "Activer MFA dans Okta"
chapter = false
weight = 81
pre = "<b>7.1 </b>"
+++
Dans ce cas d'utilisation, vous activerez MFA avec Okta Verify pour chaque connexion à Okta et donc à AWS IAM Identity Center.

### Pourquoi introduire l'AMF ?
L'identité est le nouveau périmètre et les organisations introduisent la MFA pour mieux protéger l'accès aux applications et aux services.

### Pourquoi Okta ?
Il ne suffit pas d'avoir une solution MFA, les organisations doivent pouvoir l'intégrer de manière sécurisée pour toutes les applications. Okta fournit plus de 7 000 intégrations SSO pour les applications cloud et sur site. Okta protège toutes ces applications avec MFA et si vous ne les trouvez pas sur l'{{% button href="https://www.okta.com/integrations/" %}}Okta Integration Network (OIN){{% /button %}}, Okta prend en charge les standards ouverts et d'autres méthodes d'intégration.

L'introduction d'un deuxième facteur ajoute des frictions à l'expérience de l'utilisateur final. Avec l'{{% button href="https://www.okta.com/fr/products/adaptive-multi-factor-authentication/" %}}Authentification multifacteur adaptative Okta{{% /button %}}, les organisations définissent en fonction du risque et du contexte le juste équilibre entre sécurité et expérience utilisateur.
![Adaptive MFA](/images/7_adaptive_mfa.png)

Okta fournit une {{% button href="https://www.okta.com/fr/products/adaptive-multi-factor-authentication/" %}} grande variété de facteurs neutres vis-à-vis du fournisseur{{% /button %}}. En voici quelques-uns :
- Okta Verify : application pour smartphone pour Android et iOS prenant en charge la notification push, facile à utiliser, et l’OTP
- U2F, FIDO2 & WebAuth : par ex. authentification biométrique avec Apple TouchID, Windows Hello et YubiKey
- Authentification Google
- Magic Link et OTP par e-mail
- OTP par SMS
- Intégration des tokens matériels existants, des solutions MFA héritées et OATH-OTP
- Authentification sans mot de passe, certificats et plus

### Étapes de configuration: ajouter le facteur *Okta Verify*

1. Ouvrez la console d'administration Okta et allez dans **Security** -> **Authenticator** et cliquez sur **Add Authenticator**.
![Add Authenticator](/images/740_add_authenticator.png)

2. Sélectionnez **Add** pour **Okta Verify**. Okta supporte plus d'authentificateurs que ceux présentés ici, mais ils ne sont pas disponibles dans le cadre de l'essai gratuit.
Si vous avez un MacBook avec TouchID, WindowsHello ou une clé compatible FIDO comme une YubiKey, vous pouvez également activer **FIDO2 (WebAuthn)**.
![Authenticator](/images/741_authenticators.png)

3. Sélectionnez dans la boîte de dialogue de configuration d'Okta Verify

- **Push notification (Android and iOS only)** : Cela permettra d'utiliser une notification push à côté d'un OTP avec l'application Okta Verify sur iOS et Android.
- **Okta FastPass (All platforms)** : Ceci permettra de se connecter sans mot de passe avec l'application gratuite *Okta Verify* disponible sur Mac, Windows, iOS et Android.
- **Show the "Sign in with OktaFastpass" button** : Cela permettra de se connecter sans mot de passe avec *Okta Verify* sans entrer de nom d'utilisateur ou de mot de passe.
![Configuration d'Okta Verify](/images/742_okta_verify_setup.png)

4. Une fois que l'enrôlement MFA est autorisé, il peut être configuré dans l'onglet **Factor Enrollment**. Une configuration par défaut est fournie et ça convient pour l'atelier.

### Étapes de configuration: ajouter une politique Single Sign-On dans *AWS IAM Identity Center*

L'étape suivante consiste à appliquer l'authentification MFA lors de la connexion à Okta. 
1. Allez dans **Applications** -> **Applications** et sélectionnez l'application **AWS IAM Identity Center**.

2. Passez à l’onglet **Sign On**. Défilez vers le bas et cliquez sur **View policy details**.
![AWS IAM Identity Center App Sign-On Policy](/images/743_aws_sso_sign_on_policy.png)

3. Une politique par défaut (**Default Policy**) a été automatiquement attribuée à l'application AWS IAM Identity Center.
Cette politique est partagée par plusieurs applications. Pour des raisons de simplicité, nous allons appliquer le MFA à toutes les applications, mais vous pouvez également créer une politique dédiée uniquement à l'application AWS IAM Identity Center.

4. Cliquez sur **Add rule**.
![Default Policy Add Rule](/images/744_default_policy_add_rule.png)

5. Entrez le nom de la règle **MFA for Everyone**.
![App Sign-On Policy Name](/images/745_app_sign_on_rule_name.png)

6. Sélectionnez **Possesion Factor**. Okta affichera automatiquement tous les authentificateurs activés dans votre tenant Okta qui ont le type de facteur selectionné.
![App Sign-On Policy Then](/images/746_app_sign_on_rule_then.png)

7. Pour appliquer le MFA à chaque connexion, sélectionnez **Every sign-in attempt** et cliquez sur **Save**.
![App Sign-On Policy Reauthentication](/images/747_app_sign_on_rule_reauthentication.png)

8. C'est tout. Okta vous demandera lors de la prochaine connexion d'enregistrer votre MFA (*Okta Verify*) et vous devrez l'utiliser lors des connexions suivantes.

### Test
1. Allez au tableau de bord de l'utilisateur final.
![Okta End User Dashboard](/images/280_open_end_user_dashboard.png)

2. Cliquez sur l'application **AWS IAM Identity Center**.
![Start AWS IAM Identity Center App](/images/290_start_aws_sso_app.png)

3. La première fois que vous vous connectez, vous serez invité à vous inscrire à votre MFA (*Okta Verify*).
![Setup Okta Verify](/images/703_setup_okta_verify.png)