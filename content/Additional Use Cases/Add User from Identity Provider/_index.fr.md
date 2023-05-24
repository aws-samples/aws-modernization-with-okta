+++
title = "Ajouter un utilisateur à partir d'un fournisseur d'identité"
chapter = false
weight = 85
pre = "<b>7.4 </b>"
+++

Dans ce cas d'utilisation, nous expliquerons comment utiliser un fournisseur d'identité en tant que source d'utilisateurs. Nous ne ferons pas l'intégration complète, mais nous examinerons les possibilités et les cas d'utilisation courants.

### Pourquoi utiliser un fournisseur d'identité (IdP) ?
Les fournisseurs d'identité sont utilisés pour permettre la connexion à Okta et donc à AWS IAM Identity Center avec les comptes existants de **Google**, **ADFS**, **Facebook**, etc.

### Comment se passe la connexion avec un IdP ?
L'expérience de connexion peut être conçue de plusieurs manières, comme vous pouvez le voir dans la capture d'écran suivante :
- **Règles de routage/IdP Discovery** : L'utilisateur entre son nom d'utilisateur ou son adresse e-mail et les règles définissent le fournisseur d'identité. Vous pouvez voir que le champ pour saisir le mot de passe n'est pas affiché, car cela n'a aucun sens si l'utilisateur est routé vers un fournisseur d'identité. Les règles peuvent être par exemple un nom de domaine, par ex. tous les utilisateurs avec *@partner.com* seront redirigés vers un fournisseur d'identité spécifique d'un partenaire.
- **Boutons** : l'utilisateur clique sur un bouton comme indiqué dans la capture d'écran pour s'inscrire ou se connecter lui-même, par ex. **Carte à puce**, **Facebook** ou **Google**.

![Login Widget IdP Buttons](/images/725_login_widget_IdP_buttons.png)

### Étapes de configuration
1. Les fournisseurs d'identité sont configurés dans **Security** -> **Identity Providers**. Okta fournit une intégration prête à l'emploi avec plusieurs IdP.{{% button href="https://developer.okta.com/docs/guides/add-an-external-idp/saml2/configure-idp-in-okta/" %}}Voici les instructions pour les configurer{{% /button %}}
![Add Identity Provider](/images/720_add_identity_provider.png)

2. Cliquez sur **Add Identity Provider** pour visualiser la liste des IdP supportés.
![Add Identity Provider](/images/720_add_identity_provider.png)
![IDP Selection](/images/720_01_idp_selection.png)

3. L'étape suivante consiste à créer une règle de routage. Sur la même page, passez à l’onglet **Routing Rules** et cliquez sur **Add Routing Rule** pour en créer une.
![Add Routing Rule](/images/721_add_routing_rule.png)

4. Voici un exemple de règle de routage. Chaque utilisateur qui se connecte avec **Google** ou **Okta** sera autorisé.
![Create Routing Rule](/images/728_IdP_Rule_Okta_or_Google.png)

5. Une fenêtre s'ouvre pour activer la nouvelle règle, cliquez sur **Activate**.
![Activate Routing Rule](/images/723_activate_routing_rule.png)

6. Après avoir activé la règle de routage, vous pouvez voir que le champ **Sign in with Google** est disponible.
![Login with Google IdP](/images/727_login_with_google_idp.png)