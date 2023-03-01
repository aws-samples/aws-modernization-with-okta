+++
title = "Attribuer des permissions"
chapter = false
weight = 62
+++
Sélectionnez **AWS Account**, sélectionnez un compte AWS et cliquez sur **Assign users**.

![Select Accounts](/images/select_accounts.png)

Passez à l'onglet **Groups**, sélectionnez **AWS ViewOnlyAccess** et cliquez sur **Next**. Les deux groupes affichés sont ceux que nous avons provisionnés depuis Okta à AWS IAM Identity Center.

![Assign group select group](/images/assign_group_select_group.png)

Sélectionnez la permission **ViewOnlyAccess** que nous avons créée précédemment et cliquez sur **Done**.
![Assign group select permission set](/images/assign_group_select_permission_set.png)

Attendez un instant et cliquez sur **Proceed to AWS accounts**.
![Complete assign group](/images/complete_assigned_group.png)

Répétez les mêmes étapes pour **AWS PowerUserAccess** avec le groupe et les permissions correspondantes.

Validez votre configuration : vous disposerez de deux permissions qui sont attribuées au compte AWS via des groupes.
![Validate AWS Account Configuration](/images/validate_aws_account_configuration.png)
