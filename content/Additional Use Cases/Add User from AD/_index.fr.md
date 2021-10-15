+++
title = "Ajouter un utilisateur depuis AD"
chapter = false
weight = 84
+++
Dans ce cas d'utilisation, nous verrons comment utiliser AD ou LDAP comme source d'utilisateurs. Nous ne ferons pas l'intégration complète, mais nous examinerons les possibilités et les cas d'utilisation courants.

Allez dans “Directory” -> “Directory Integrations” et cliquez sur “Add Active Directory”.

![Add AD](/images/710_add_active_directory.png)

La page suivante montrera l'architecture de haut niveau de l'intégration.

![Integration](/images/713_integration_short.png)

Le ou les contrôleurs de domaine AD sont généralement déployés derrière un pare-feu. Okta utilise un agent léger pour l'intégration qui offre de nombreux avantages :
- L'agent AD n'a qu'une connexion sortante vers Okta via le protocole chiffré HTTPS. Cela signifie que les organisations n'ont pas à ouvrir leurs pare-feux.
- Il est recommandé d'installer l'agent AD sur un serveur joint au domaine. Il ne doit pas s'exécuter sur le contrôleur de domaine.
- La configuration se fait dans l’interface web d’Okta (“Directory” -> “Directory Integrations”). Aucun accès au serveur Windows n'est requis après l'installation.
- Okta peut importer des utilisateurs et des groupes depuis AD. Les groupes importés et leurs membres sont affichés dans “Directory” -> “People”. Il est possible de définir des modèles pour faire automatiquement correspondre des utilisateurs importés à des utilisateurs Okta existants, ou d’utiliser l’interface Web pour résoudre les conflits.
- Okta peut créer, mettre à jour et désactiver des utilisateurs dans AD ainsi que gérer l'appartenance à un groupe AD.
- Okta prend en charge les attributs personnalisés et vous contrôlez totalement les attributs lus ou écrits dans “Directory” -> “Profile Editor”. Vous pouvez même utiliser le langage d'expression d'Okta pour transformer les attributs pour des cas d'utilisation plus complexes.
- Okta prend en charge plusieurs AD et LDAP. Si l'utilisateur existe dans plusieurs répertoires, vous pouvez définir la priorité dans “Directory” -> “Profile Sources”. Vous pouvez même définir la source par attribut, par ex. vous pouvez définir un AD spécifique pour être la source du département de tous les utilisateurs.
- Okta prend en charge l'authentification déléguée. Cela signifie que le mot de passe est validé dans l'AD et non dans Okta, de sorte que l'utilisateur peut se connecter avec le même mot de passe qu'il connaît déjà.
- Okta fournit des fonctionnalités en libre-service pour la réinitialisation du mot de passe et le déverrouillage du compte pour les utilisateurs AD.
- Okta prend en charge le provisionnement Just-In-Time (JIT), de sorte que tous les utilisateurs n'ont pas besoin d'être importés en premier lieu et que les dernières données sont importées lors de la connexion.
- Okta prend en charge l'authentification unique de bureau sans agent. Si les utilisateurs proviennent d'un appareil appartenant à un domaine, ils seront automatiquement connectés à Okta sans saisir leur nom d'utilisateur et leur mot de passe. Comme son nom l'indique, aucun agent supplémentaire n'est requis sur l'appareil de l'utilisateur.

Les prochaines étapes de l'intégration AD dépassent le cadre de cet atelier. Pour les instructions plus détaillées, vous pouvez consulter la documentation officielle [ici](https://help.okta.com/en/prod/Content/Topics/Directory/ad-agent-workflow.htm).
