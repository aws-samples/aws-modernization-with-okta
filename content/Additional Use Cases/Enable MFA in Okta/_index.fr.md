+++
title = "Activer MFA dans Okta"
chapter = false
weight = 81
+++
Dans ce cas d'utilisation, vous activerez MFA avec Okta Verify pour chaque connexion à Okta et donc à AWS SSO.

### Pourquoi introduire l'AMF ?
L'identité est le nouveau périmètre et les organisations introduisent la MFA pour mieux protéger l'accès aux applications et aux services.

### Pourquoi Okta ?
Il ne suffit pas d'avoir une solution MFA, les organisations doivent pouvoir l'intégrer de manière sécurisée pour toutes les applications. Okta fournit plus de 7 000 intégrations SSO pour les applications cloud et sur site. Okta protège toutes ces applications avec MFA et si vous ne les trouvez pas sur l'{{% button href="https://www.okta.com/integrations/" %}}Okta Integration Network (OIN){{% /button %}}, Okta prend en charge les standards ouverts et d'autres méthodes d'intégration.

L'introduction d'un deuxième facteur ajoute des frictions à l'expérience de l'utilisateur final. Avec l'{{% button href="https://www.okta.com/products/adaptive-multi-factor-authentication/" %}}Authentification multifacteur adaptative Okta{{% /button %}}, les organisations définissent en fonction du risque et du contexte le juste équilibre entre sécurité et expérience utilisateur.

Okta fournit une {{% button href="https://www.okta.com/products/adaptive-multi-factor-authentication/" %}} grande variété de facteurs neutres vis-à-vis du fournisseur{{% /button %}}. En voici quelques-uns :
- Okta Verify : application pour smartphone pour Android et iOS prenant en charge la notification push, facile à utiliser, et l’OTP
- U2F, FIDO2 & WebAuth : par ex. authentification biométrique avec Apple TouchID, Windows Hello et YubiKey
- Authentification Google
- Magic Link et OTP par e-mail
- OTP par SMS
- Intégration des tokens matériels existants, des solutions MFA héritées et OATH-OTP
- Authentification sans mot de passe, certificats et plus

### Étapes de configuration

Ouvrez la console d'administration Okta et allez dans "Security" -> "Multifactor".
Sélectionnez "Okta Verify", réglez-le sur "Active" et définissez au moins "Enable Push Notification". Enregistrez les paramètres.
![Enable Multifactor Okta Verify](/images/700_enable_multifactor_okta_verify.png)

L’inscription MFA autorisée peut être configurée dans l’onglet “Factor Enrollment”. La configuration par défaut fournie peut être utilisée pour cet atelier.

L'étape suivante consiste à appliquer l'authentification MFA lors de la connexion à Okta. Allez dans “Security” -> “Authentication” et passez à l’onglet “Sign On”. Une politique par défaut est déjà fournie pour tous les utilisateurs. Cliquez sur “Add Rule”.

![Add SSO Rule](/images/701_add_sso_rule.png)

Entrez le nom de la règle "MFA pour tout le monde", sélectionnez “Prompt for Factor”, sélectionnez “Every Time” et cliquez sur “Create Rule”.

![Add MFA Rule](/images/702_add_mfa_rule.png)

C'est terminé. Okta vous demandera lors de la prochaine connexion de paramétrer votre MFA (Okta Verify) et lors des connexions suivantes, vous devrez l'utiliser.

![Setup Okta Verify](/images/703_setup_okta_verify.png)
