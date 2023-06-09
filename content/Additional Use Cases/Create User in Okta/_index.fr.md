+++
title = "Créer un utilisateur dans Okta"
chapter = false
weight = 83
pre = "<b>7.2 </b>"
+++
Dans ce cas d'utilisation, nous allons créer un nouvel utilisateur dans Okta et fournir un accès à AWS IAM Identity Center.

### Pourquoi gérer les utilisateurs directement dans Okta ?
La gestion des utilisateurs directement dans Okta résout le problème qui se pose lorsque les organisations souhaitent fournir un accès aux ressources AWS aux partenaires, mais ne souhaitent pas les créer dans AD.

### Étapes de configuration
1. Pour créer un nouvel utilisateur dans Okta, allez dans **Directory** -> **People** et cliquez sur **Add person**.
![Add People](/images/730_add_people.png)

2. Entrez les informations sur l'utilisateur. Pour fournir l'accès à AWS, commencez à saisir le nom du groupe **AWS ViewOnlyAccess** et sélectionnez-le. Assurez-vous que l'option **Activate now** est sélectionnée. Cela activera l'utilisateur dans Okta et un e-mail pour définir le mot de passe initial sera envoyé à l'utilisateur. Cliquez sur **Save**.

{{% notice info %}}
Si vous ne sélectionnez pas **Send user activation email now**, Okta crée l'utilisateur dans un état Staged et vous devez l'activer manuellement.
Des attributs utilisateur supplémentaires peuvent être définis dans l'onglet Profil de l'utilisateur.
{{% /notice %}}

![Send User Actication Email](/images/731_send_user_activation_email.png)

3. Cliquez sur le lien dans l'e-mail d'activation que vous avez reçu dans votre boîte aux lettres et définissez le mot de passe.

4. Déconnectez-vous avec votre utilisateur actuel ou ouvrez un nouveau navigateur incognito. Connectez-vous avec le nouvel utilisateur comme décrit dans le chapitre **Test** depuis Okta ou AWS. Vous serez invité à paramétrer votre MFA et comme nous n'avons attribué qu'un seul groupe, vous n'aurez accès qu'à **ViewOnlyAccess**.
(La capture d'écran montre également **PowerUserAccess**)
![AWS Dashboard new Okta user](/images/732_aws_dashboard.png)

### Nettoyage

1. Pour désactiver l'utilisateur et supprimer l'accès à AWS IAM Identity Center, accédez à **Directory** -> **People** et cliquez sur le nom d'utilisateur.
![Select User](/images/733_select_user.png)

2. Cliquez sur **More Actions** et **Deactivate**.
![Deactivate User](/images/734_deactivate_user.png)

{{% notice info %}}
Okta désactive les utilisateurs en premier lieu, car la suppression d'un utilisateur peut avoir un impact important, par ex. que se passe-t-il avec les fichiers personnels de l'utilisateur dans un lecteur cloud intégré à Okta ? Le gestionnaire doit-il avoir accès aux fichiers, les fichiers doivent-ils être supprimés ? Pour automatiser le parcours complet de l'utilisateur, Okta propose un outil no-code, [Workflows](https://www.okta.com/fr/platform/workflows/workflows-for-lifecycle-management/), pour définir des actions granulaires fines.
{{% /notice %}}

{{% notice info %}}
Si vous souhaitez supprimer l'utilisateur, cliquez sur le bouton **Delete** dans le profil utilisateur qui s'affiche après la désactivation.
![Delete User](/images/736_delete_user.png)
{{% /notice %}}
