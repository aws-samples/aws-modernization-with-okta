+++
title = "Déployer des groupes"
chapter = false
weight = 52
+++
AWS IAM Identity Center ne connaît pas encore nos groupes. Nous utiliserons les groupes pour mapper les permissions (**Permission Sets**) dans AWS IAM Identity Center. Déployons les groupes et leurs adhésions vers AWS IAM Identity Center.

1. Allez dans l'onglet **Push Groups** et cliquez sur **Find groups by name**. Si vous avez plus de groupes, vous pouvez également utiliser **Find groups by rule**. Mais restons simples pour cet atelier.
![Start Push Groups Configuration](/images/240_start_push_groups_configuration.jpg)

2. Entrez **aws** dans le champ de recherche et sélectionnez **AWS PowerUserAccess**. Si le nom du groupe n'existe pas encore dans AWS IAM Identity Center, Okta en créera un nouveau. Sinon, un groupe existant sera lié.
![Push Groups aws PowerUserAccess](/images/250_push_group_aws_powerUserAccess.png)

3. Assurez-vous de sélectionner **Push group memberships immediately**. Cliquez sur **Save & Add Another**. 
![Push Groups Save and add another](/images/260_push_groups_save_and_add_another.png)

4. Répétez la même étape pour **AWS ViewOnlyAccess**.

5. Assurez-vous que **Push Status** est bien **Active**. La configuration ressemblera à celle ci-dessous :
![Verify Push Grup Configuration](/images/270_verify_push_group_configuration.png)
