+++
title = "Nettoyage"
chapter = true
weight = 90
+++
Si vous avez réalisé cet atelier à des fins d'apprentissage et non pour la production, vous devez toujours supprimer les ressources créées une fois toutes les étapes terminées.
Dans le compte AWS, accédez aux paramètres sous le service SSO et cliquez sur **Supprimer la configuration AWS IAM Identity Center**. Vous devez confirmer que vous comprenez que tout ce qui concerne l'authentification unique (y compris les utilisateurs et les groupes poussés) sera supprimé en sélectionnant les cases et en écrivant **SUPPRIMER** (**DELETE** en anglais) dans la zone de texte.

![Delete SSO](/images/delete_sso.png)

Le nettoyage dans Okta pour un compte développeur gratuit n'est pas requis, car aucune dépense supplémentaire n'est générée. Néanmoins, il est recommandé de supprimer les utilisateurs et les applications inutilisés dans Okta. Pour supprimer l'application AWS IAM Identity Center, allez dans le tableau de bord d'administration Okta dans **Applications** -> **Applications** et désactivez et supprimez **AWS IAM Identity Center**. Si vous avez créé des utilisateurs supplémentaires, allez dans **Directory** -> **People**, désactivez-les et supprimez-les.

![Deactivate AWS IAM Identity Center Application](/images/500_Delete_AWS_SSO.png)

![Delete AWS IAM Identity Center Application](/images/510_Delete_AWS_SSO.png)
