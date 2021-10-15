+++
title = "Assigner des utilisateurs"
chapter = false
weight = 51
+++
Pour permettre aux utilisateurs l’accès via SSO, nous devons les assigner à l'application AWS SSO dans Okta. Dès que vous assignez un utilisateur ou un groupe, Okta appellera en arrière-plan les API pour créer l'utilisateur dans AWS SSO. Si vous modifiez un attribut mappé, par ex. FirstName, Okta mettra également à jour l'attribut dans AWS SSO. Si vous désaffectez un utilisateur, il sera désactivé dans AWS SSO. Okta s'occupe de la gestion complète du cycle de vie des utilisateurs.

Allez dans l'onglet « Assignments » et cliquez sur « Assign to Groups ».
![Assign to Groups](/images/210_assign_groups.jpg)

Cliquez sur « Assign » pour les deux groupes. Une boîte de dialogue apparaîtra pour effectuer un mapping d'attributs supplémentaire par groupe. Aucun changement n'est requis, il suffit de le confirmer. Terminez l'activité en cliquant sur « Done ».
![Assign AWS Groups](/images/220_assign_each_group.png)

La configuration ressemblera à celle ci-dessous :
![Configured Groups](/images/230_validate_assignment_configuration.jpg)
