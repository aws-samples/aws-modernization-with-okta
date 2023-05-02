+++
title = "Assigner des utilisateurs"
chapter = false
weight = 51
+++
Pour permettre aux utilisateurs l’accès via SSO, nous devons les assigner à l'application AWS IAM Identity Center dans Okta. Dès que vous assignez un utilisateur ou un groupe, Okta appellera en arrière-plan les API pour créer l'utilisateur dans AWS IAM Identity Center. Si vous modifiez un attribut mappé, par ex. FirstName, Okta mettra également à jour l'attribut dans AWS IAM Identity Center. Si vous désaffectez un utilisateur, il sera désactivé dans AWS IAM Identity Center. Okta s'occupe de la gestion complète du cycle de vie des utilisateurs.

1. Allez dans l'onglet **Assignments** et cliquez sur **Assign to Groups**.
![Assign to Groups](/images/210_assign_groups.jpg)

2. Cliquez sur **Assign** pour les deux groupes. Une boîte de dialogue apparaîtra pour effectuer un mapping d'attributs supplémentaire par groupe. Aucun changement n'est requis, il suffit de le confirmer. Terminez l'activité en cliquant sur **Done**.
![Assign AWS Groups](/images/220_assign_each_group.png)

3. La configuration ressemblera à celle ci-dessous :
![Configured Groups](/images/230_validate_assignment_configuration.jpg)
