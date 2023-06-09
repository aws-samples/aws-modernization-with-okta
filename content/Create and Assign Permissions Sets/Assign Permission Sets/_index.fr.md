+++
title = "Attribuer des permissions"
chapter = false
weight = 62
pre = "<b>5.2 </b>"
+++
1. Sélectionnez **AWS Account**, sélectionnez un **AWS account** et cliquez sur **Assign users**.
![Select Accounts](/images/350_select_accounts.png)

2. Passez à l'onglet **Groups**, sélectionnez **AWS PowerUserAccess** et cliquez sur **Next**. Les deux groupes affichés sont ceux que nous avons provisionnés depuis Okta à AWS IAM Identity Center.
![Assign group select group](/images/355_assign_group_select_group.png)

3. Cliquez **Next**

4. Validez votre configuration : vous disposerez du groupe **AWS PowerUserAccess** à lequel la permission **PowerUserAccess** sera attribuée.
![Complete assign group](/images/365_complete_assigned_group.png)

5. Répétez les mêmes étapes pour **AWS ViewOnlyAccess** avec le groupe et les permissions correspondantes.

6. Validez votre configuration : vous disposerez de deux permissions qui sont attribuées au compte AWS via des groupes.
![Validate AWS Account Configuration](/images/370_validate_aws_account_configuration.png)