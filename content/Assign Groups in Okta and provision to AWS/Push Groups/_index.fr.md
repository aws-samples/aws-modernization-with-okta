+++
title = "Déployer des groupes"
chapter = false
weight = 52
+++
AWS SSO ne connaît pas encore nos groupes. Nous utiliserons les groupes pour mapper les permissions dans AWS SSO. Déployons les groupes et leurs adhésions vers AWS SSO.

Allez dans l'onglet "Push Groups" et cliquez sur "Find groups by name". Si vous avez plus de groupes, vous pouvez également utiliser "Find groups by rule". Mais restons simples pour cet atelier.
![Start Push Groups Configuration](/images/240_start_push_groups_configuration.jpg)

Entrez "aws” dans le champ de recherche et sélectionnez "AWS PowerUserAccess”.
![Push Groups aws PowerUserAccess](/images/250_push_group_aws_powerUserAccess.png)

{{% notice info %}}
Si le nom du groupe n'existe pas encore dans AWS SSO, Okta en créera un nouveau. Sinon, un groupe existant sera lié.
{{% /notice %}}

Cliquez sur "Save & Add Another". Répétez la même étape pour "AWS ViewOnlyAccess".
![Push Groups Save and add another](/images/260_push_groups_save_and_add_another.png)

La configuration ressemblera à celle ci-dessous :
![Verify Push Grup Configuration](/images/270_verify_push_group_configuration.png)
