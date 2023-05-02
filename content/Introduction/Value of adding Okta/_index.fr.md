+++
title = "Valeur ajoutée d'Okta"
chapter = false
weight = 12
+++
Lorsque les utilisateurs accèdent aux ressources AWS, les entreprises doivent s'assurer que les bonnes personnes peuvent accéder aux bonnes ressources de manière sécurisée. Les utilisateurs peuvent être des employés, des partenaires ou des clients. Leur source de vérité est leur système RH, les répertoires AD ou LDAP, l'enregistrement en libre-service ou les fournisseurs d'identité.
L'utilisation de la bonne source de vérité est essentielle pour que les organisations automatisent le processus **Joiner-Mover-Leaver** (Arrivée/Mutation/Départ) :
- **Joiner :** Un nouvel utilisateur/Une nouvelle utilisatrice rejoint l'organisation. Okta fournit un accès natif automatisé à AWS et à d'autres applications pour le/la rendre aussi productif/productive que possible dès leur premier jour.
- **Mover:** Lorsque les utilisateurs changent de travail ou de rôle, sont promus, changent de nom en raison du mariage ou partent en congé. Okta maintient les systèmes connectés synchronisés et fournit le bon accès.
- **Leaver :** À la fin du cycle de vie, l'utilisateur part immédiatement, à une certaine heure, en fonction d’une planification par le système RH ou simplement en étant désactivé dans un annuaire AD ou LDAP. Okta déprovisionne l'accès pour sécuriser les systèmes.

![Workforce Lifecycle Management](/images/1_Workforce_Lifecycle_Management.png)

L'étape suivante consiste à fournir un accès sécurisé et facile à utiliser à l'aide d'un MFA adaptatif. Okta vous permet de contrôler entièrement les politiques d'accès à AWS, telles que

- autoriser l'accès uniquement à partir d'appareils gérés par l'entreprise
- appliquer des facteurs MFA résistants à l'hameçonnage comme FIDO2 à chaque connexion
- inclure des signaux de risque pour définir l'accès en fonction du contexte de l'utilisateur, de l'appareil, de l'application, du réseau, de l'emplacement et des signaux externes.

![Adaptive MFA](/images/7_adaptive_mfa.png)

Pourquoi choisir Okta et AWS IAM Identity Center ?
- Configurez l'authentification unique et le provisionnement sur AWS IAM Identity Center avec l'application {{% button href="https://www.okta.com/integrations/" %}}Okta Integration Network (OIN){{% /button %}} préconfigurée
- Automatisez les scénarios de **Joiner-Mover-Leaver** avec les outils avancés de gestion du cycle de vie d'Okta
- Authentifiez-vous auprès d'AWS IAM Identity Center en utilisant Okta en tant que fournisseur d'identité à l'aide des nouveaux outils AWS CLI
- Ajoutez un MFA adaptatif basé sur le contexte et les risques et passez sans mot de passe avec Okta FastPass

![High Level Architecture](/images/2_High_Level_Architecture.png)

Okta et AWS IAM Identity Center offrent des moyens flexibles de contrôler :
- Gestion des accès multi-comptes et granulaire
- Contrôle d'accès basé sur les attributs via des assertions Okta ou la sélection AWS IAM Identity Center d'attributs utilisateurs qui sont synchronisés avec Okta
- Attribuez des niveaux d'autorisations dans AWS IAM Identity Center ou attribuez-les dans le cadre de la gestion du cycle de vie des utilisateurs Okta

![High Level Architecture2](/images/3_High_Level_Architecture2.png)

{{% notice tip %}}
L'intégration du centre d'identité AWS IAM n'est qu'un exemple parmi tant d'autres. {{% button href="https://www.okta.com/partners/aws" %}}Cliquez ici pour toutes les intégrations Okta avec AWS.{{% /button %}}
{{% /notice %}}