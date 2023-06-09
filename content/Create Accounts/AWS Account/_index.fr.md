+++
title = "Compte AWS"
chapter = false
weight = 22
pre = "<b>1.2 </b>"
+++
# Préparez votre compte de laboratoire

Si vous assistez à un événement organisé par AWS (tel que re:Invent, Immersion Day, atelier sur site ou autre événement organisé par des employés AWS), vous recevrez un compte AWS temporaire pour l'atelier.

Si vous suivez cet atelier vous-même, votre compte doit avoir la possibilité de créer de nouveaux rôles IAM et d'étendre d'autres autorisations IAM.

- Si vous n'avez pas encore de compte AWS avec accès administrateur : créez-en un maintenant
{{% button href="https://aws.amazon.com/getting-started/" %}}Cliquez ici pour ouvrir un compte AWS {{% /button %}}
- Vous pouvez également trouver des conseils supplémentaires sur la façon de créer un compte AWS
{{% button href="https://aws.amazon.com/premiumsupport/knowledge-center/create-and-activate-aws-account/" %}}Cliquez ici pour obtenir des conseils {{% /button %}}

{{% notice tip %}}
- Une fois que vous avez un compte AWS, assurez-vous de créer un utilisateur IAM en lui rattachant la politique AdministratorAccess. Vous utiliserez ce compte pour l'atelier. En tant que bonne pratique, n'utilisez JAMAIS le compte racine AWS lorsque vous pouvez utiliser un utilisateur IAM à la place !
{{% /notice %}}