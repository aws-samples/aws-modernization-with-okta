+++
title = "Créer des permissions"
chapter = false
weight = 61
pre = "<b>5.1 </b>"
+++
1. Accédez à AWS **IAM Identity Center**.
![Create Permission Set](/images/go_to_aws_sso.png)

2. Sélectionnez **Permission sets** et **Create permission set**
![Create Permission Set](/images/300_create_permission_set.png)

3. Vous pouvez choisir entre des jeux de permissions: *predefined* ou *custom*. Pour cet atelier, nous nous en tenons à la simplicité. Sélectionnez **Predefined permission set** et **PowerUserAccess**. Cliquez sur **Next**.
![Create Permission Type](/images/305_create_permission_type.png)

4. Cliquez sur **Next** et sur la dernière page sur **Create**.

5. Répétez les mêmes étapes pour **AWS PowerUserAccess** avec les role policies correspondantes.

6. Validez votre configuration : vous disposerez de deux permissions qui seront attribuées aux groupes correspondants d’Okta.
![Validate Permission Sets](/images/310_validate_permission_sets.png)