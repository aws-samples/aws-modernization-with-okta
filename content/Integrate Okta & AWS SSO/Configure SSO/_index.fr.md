+++
title = "Configurer l'authentification unique (SSO)"
chapter = false
weight = 42
+++
Sélectionnez l'onglet « Sign On » puis sur « View Setup Instructions ».
Suivez les instructions. Les valeurs dans les instructions sont générées spécifiquement pour votre tenant Okta.
Pour la partie des métadonnées, vous pouvez l'ouvrir sur un nouvel onglet de navigateur et télécharger le fichier metadata.xml.

![Sign On Configuration](/images/180_sign_on_configuration.jpg)

{{%attachments style="green" title="Exemple de configuration générée par Okta" pattern=".*(pdf)"/%}}

{{% notice tip %}}
Le document attaché est un fichier d'exemple qui a été créé pour cet atelier. Ces fichiers sont créés dynamiquement et spécifiquement pour votre tenant, alors assurez-vous d'utiliser le vôtre et non ce fichier d'exemple.
{{% /notice %}}

{{% notice warning %}}
Une organisation AWS est obligatoire pour activer AWS IAM Identity Center. Si vous n'en avez pas lorsque vous activez AWS IAM Identity Center, vous pourrez être invité à créer une AWS Organization.
Vous trouverez des informations plus détaillées sur la façon de configurer l'organisation AWS dans le lien ci-dessous :
[AWS: Création et configuration d'une organisation](https://docs.aws.amazon.com/fr_fr/organizations/latest/userguide/orgs_tutorials_basic.html)
{{% /notice %}}
