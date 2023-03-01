+++
title = "Accès à l'AWS CLI"
chapter = false
weight = 88
+++
Dans ce cas d'utilisation, vous vous connecterez à l'AWS CLI avec Okta via AWS IAM Identity Center.

AWS CLI v2 prend en charge l'intégration directe avec AWS IAM Identity Center. Vous pouvez désormais créer des profils CLI liés aux comptes et rôles SSO. L'interface de ligne de commande récupère automatiquement les informations d'identification AWS à partir de l'authentification unique et les actualise en votre nom. De nouvelles commandes aident à gérer les profils CLI SSO. Vous n'avez plus besoin de copier et coller les informations d'identification AWS temporaires à partir de la console AWS IAM Identity Center.

Exécutez dans un terminal ***aws configure sso*** et suivez les instructions.
- **SSO start URL** : connectez-vous au tableau de bord AWS et copiez l'URL.
- **SSO Region** : connectez-vous à votre compte AWS et copiez la région d'AWS IAM Identity Center.

{{< highlight ssh >}}
$ aws configure sso
{{< / highlight >}}

Le résultat sera
{{< highlight ssh >}}
$ aws configure sso
SSO start URL [None]: https://d-99xxxxxx75.awsapps.com/start
SSO Region [None]: eu-central-1

Attempting to automatically open the SSO authorization page in your default browser.
If the browser does not open or you wish to use a different device to authorize this request, open the following URL:

https://device.sso.eu-central-1.amazonaws.com/

Then enter the code:

RXPC-JNHZ
The only AWS account available to you is: 00xxxxxxxx56
Using the account ID  00xxxxxxxx56
{{< / highlight >}}

Vous serez invité à vous connecter à votre AWS IAM Identity Center via Okta. Si vous avez activé MFA, vous devez également fournir un 2e facteur. De plus, vous serez également invité par AWS IAM Identity Center à autoriser l'accès.

![AWS CLI Authorize Request](/images/aws_cli_authorize_request.png)

Après une authentification réussie, vous serez invité à sélectionner l'un des rôles que nous configurons dans le cadre de l'atelier. Sélectionnez l'un d'eux pour créer un profil local.

{{< highlight ssh >}}
There are 2 roles available to you.
> PowerUserAccess
  ViewOnlyAccess

Using the role name "PowerUserAccess"
CLI default client Region [eu-central-1]:                                                             
CLI default output format [None]: json                                         
CLI profile name [PowerUserAccess-00xxxxxxxx56]:
{{< / highlight >}}

Pour tester le profil, exécutez ***aws sts get-caller-identity --profile profilenameABC***

Par exemple, dans notre cas, nous avons utilisé la commande :
{{< highlight ssh >}}
$ aws sts get-caller-identity --profile PowerUserAccess-00xxxxxxxx56
{{< / highlight >}}

Le résultat sera
{{< highlight ssh >}}
$ aws sts get-caller-identity --profile PowerUserAccess-00xxxxxxxx56
{
    "UserId": "AROAXXXXXXXXXXXXXUN6N:name@domain.com",
    "Account": "00xxxxxxxx56",
    "Arn": "arn:aws:sts::00xxxxxxxx56:assumed-role/AWSReservedSSO_PowerUserAccess_7aXXXXXXXXXXXX17/name@domain.com"
}
{{< / highlight >}}

Ce cas d'utilisation est basé sur {{% button href="https://www.okta.com/blog/2020/05/how-okta-aws-sso-simplifies-admin-and-adds-cli-support/" %}} cet article {{% /button %}} et {{% button href="https://aws.amazon.com/blogs/developer/aws-cli-v2-now-supports-aws-single-sign-on/" %}}cet article {{% /button %}} de blog. Bravo à ces auteurs !
