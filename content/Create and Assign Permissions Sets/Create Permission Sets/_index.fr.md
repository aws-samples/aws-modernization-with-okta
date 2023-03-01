+++
title = "Créer des permissions"
chapter = false
weight = 61
+++
Accédez à AWS IAM Identity Center.

![Create Permission Set](/images/go_to_aws_sso.png)

Sélectionnez **AWS accounts**, cliquez sur **Permission sets** et **Create permission set**

![Create Permission Set](/images/create_permission_set.png)

L'assistant propose plusieurs options. Pour cet atelier, nous utilisons une role policy existante. Il existe plusieurs rôles **communs** déjà configurés, mais vous pouvez toujours créer une permission personnalisée avec les policies managées par AWS ou même avec votre propre policy document.

Sélectionnez **Use an existing job function policy** et cliquez sur **Next**.

![Create Permission Type](/images/create_permission_type.png)

Sélectionnez **ViewOnlyAccess** et cliquez sur **Next**.

![Create Permission Details](/images/create_permission_details.png)

Cliquez sur **Next** et sur la dernière page sur **Create**.

![Create Permission Review](/images/create_permission_review.png)

Répétez les mêmes étapes pour **AWS PowerUserAccess** avec les role policies correspondantes.

Validez votre configuration : vous disposerez de deux permissions qui seront attribuées aux groupes correspondants d’Okta.
![Validate Permission Sets](/images/validate_permission_sets.png)
