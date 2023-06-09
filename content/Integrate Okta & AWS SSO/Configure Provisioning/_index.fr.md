+++
title = "Configurer l'approvisionnement"
chapter = false
weight = 43
pre = "<b>3.3 </b>"
+++

1. Allez sur **AWS Management console** et sélectionnez l'onglet **IAM Identity Center**.
![AWS IAM Identity Center User portal](/images/go_to_aws_sso.png)

2. Sélectionnez **Settings** et **Enable** dans l'onglet *« Automatic provisioning »*.
![Enable Provisioning](/images/192_enable_provisioning.png)

3. Copiez les valeurs de **SCIM endpoint** et **Access token**.
![Copy SCIM Endpoint](/images/191_copy_scim_endpoint.png)

4. Allez sur la console *Okta* et sélectionnez l'onglet **Provisioning**. Cliquez sur **Configure API Integration**.
![Configure API Integration](/images/193_configure_api_integration.png)

5. Collez les deux valeurs copiées (**SCIM endpoint** et **Access token**) et cliquez sur **Test API Credentials**. Lorsque vous copiez l'URL, assurez-vous qu'il n'y a pas de **/** à la fin, sinon la validation du lien dans Okta échouera. Cliquez sur **Save**.
![Provisioning Configuration](/images/194_provisioning_configuration.png)

6. Dans l'onglet **Provisioning**, assurez-vous que **To App** est sélectionné. Dans le coin supérieur droit, cliquez sur **Edit** et sélectionnez **Enable** pour **créer**, **mettre à jour** et **désactiver** les utilisateurs. Cliquez sur **Save**.
![Configure Provisioning](/images/200_enable_provisioning.png)