+++
title = "Créer des groupes Okta"
chapter = true
weight = 30

+++
L'attribution des permissions dans AWS SSO peut être configurée par utilisateur. Cependant, pour être plus flexible, nous allons créer et utiliser des groupes.

Nous allons créer deux groupes dans Okta pour cet atelier : « AWS PowerUserAccess » et « AWS ViewOnlyAccess ». Les utilisateurs seront gérés dans Okta et automatiquement provisionnés sur AWS SSO.

{{% notice info %}}
Nous utiliserons des groupes gérés dans Okta, mais comme vous pouvez le voir sur la capture d'écran, les groupes sont pris en charge à partir de plusieurs sources, par ex. AD, LDAP, Workday, Google, Microsoft365. En plus de cela, vous pouvez également créer des groupes dynamiquement assignés dans Okta, par ex. en fonction des attributs de l'utilisateur tels que le Département.
![Okta Group Sources](/images/40_okta_groups_sources.jpg)
{{% /notice %}}

{{% notice info %}}
Les utilisateurs d'Okta peuvent provenir de plusieurs sources. Comme vous pouvez le voir dans la capture d'écran suivante, les utilisateurs sont pris en charge par Workday, AD, ADFS ainsi que par plusieurs AD, plusieurs LDAP, Google, etc. Cela signifie que si un utilisateur est désactivé dans AD, Okta prendra soin de désactiver l'utilisateur dans AWS SSO et d'autres applications (si pris en charge par l'application).
![Okta User Sources](/images/50_okta_user_sources.png)
{{% /notice %}}
