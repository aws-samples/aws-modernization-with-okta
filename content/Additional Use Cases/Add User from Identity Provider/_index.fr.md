+++
title = "Ajouter un utilisateur à partir d'un fournisseur d'identité"
chapter = false
weight = 85
+++

Dans ce cas d'utilisation, nous expliquerons comment utiliser un fournisseur d'identité en tant que source d'utilisateurs. Nous ne ferons pas l'intégration complète, mais nous examinerons les possibilités et les cas d'utilisation courants.

### Pourquoi utiliser un fournisseur d'identité (IdP) ?
Les fournisseurs d'identité sont utilisés pour permettre la connexion à Okta et donc à AWS SSO avec les comptes existants de Google, ADFS, Facebook, etc.

### Comment se passe la connexion avec un IdP ?
L'expérience de connexion peut être conçue de plusieurs manières, comme vous pouvez le voir dans la capture d'écran suivante :
- Règles de routage/IdP Discovery : L'utilisateur entre son nom d'utilisateur ou son adresse e-mail et les règles définissent le fournisseur d'identité. Vous pouvez voir que le champ pour saisir le mot de passe n'est pas affiché, car cela n'a aucun sens si l'utilisateur est routé vers un fournisseur d'identité. Les règles peuvent être par exemple un nom de domaine, par ex. tous les utilisateurs avec @partner.com seront redirigés vers un fournisseur d'identité spécifique d'un partenaire.
- Boutons : l'utilisateur clique sur un bouton comme indiqué dans la capture d'écran pour s'inscrire ou se connecter lui-même, par ex. Carte à puce, Facebook ou Google.

![Login Widget IdP Buttons](/images/725_login_widget_IdP_buttons.png)

### Étapes de configuration
Les fournisseurs d'identité sont configurés dans “Security” -> “Identity Providers”. Okta fournit une intégration prête à l'emploi avec plusieurs IdP.{{% button href="https://developer.okta.com/docs/guides/add-an-external-idp/saml2/configure-idp-in-okta/" %}}Voici les instructions pour les configurer{{% /button %}}

![Add Identity Provider](/images/720_add_identity_provider.png)

L'étape suivante consiste à créer une règle de routage. Sur la même page, passez à l’onglet “Routing Rules” et cliquez sur “Add Routing Rule” pour en créer une.

![Add Routing Rule](/images/721_add_routing_rule.png)

Voici un exemple de règle de routage. Chaque utilisateur qui se connecte avec @gmail.com sera redirigé vers “My Google IdP”.

![Configure Routing Rule](/images/722_configure_routing_rule.png)

Après avoir créé la règle, vous devez l'activer.
{{% notice warning %}}
Assurez-vous que votre utilisateur administrateur ne correspond PAS à la règle ou vous pourriez vous verrouiller.
{{% /notice %}}

![Activate Routing Rule](/images/723_activate_routing_rule.png)

Après avoir activé la règle de routage, vous pouvez voir que le champ pour saisir le mot de passe n'est plus affiché.
![Username only login Widget](/images/724_username_only_login_widget.png)

Pour afficher les boutons des fournisseurs d'identité (par exemple, connectez-vous avec Google), vous disposez des options suivantes :
- Domaine URL personnalisé : Allez dans “Settings” -> “Customization” et passez par l’assistant de “Custom URL Domain”. Cela vous permettra de configurer le widget de connexion hébergé Okta pour ajouter l'IdP dans “Settings” -> “Customization” et d’aller dans l’onglet “Custom Sign In”.
- Widget de connexion hébergé Okta personnalisé : intégrez le widget de connexion Okta sur votre propre site Web comme décrit{{% button href="https://developer.okta.com/code/javascript/okta_sign-in_widget/" %}}ici{{% /button %}}.

![Custom URL Domain](/images/726_custom_URL_domain.png)
