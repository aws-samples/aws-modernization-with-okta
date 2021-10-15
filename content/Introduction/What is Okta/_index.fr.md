+++
title = "Qu'est-ce qu'Okta?"
chapter = false
weight = 11
+++
Okta est une plateforme de confiance pour sécuriser toutes vos identités.

Okta est un service de gestion d'identité, construit dans le cloud pour le cloud, mais également compatible avec de nombreuses applications on-premises. Avec Okta, un département informatique peut gérer l'accès de n'importe quel/quelle employé(e) à n'importe quelle application ou appareil. Okta fonctionne dans le cloud, sur une plateforme sécurisée, fiable et activement auditée, qui s'intègre aux applications, annuaires et systèmes de gestion des identités dans le cloud et sur site.

La solution Okta est née des défis uniques liés à la façon dont la technologie s'est développée et a évolué dans une diversité croissante d'appareils, de problèmes d'identité, de sécurité, de mobilité des employés/employées, de partenariats avec des fournisseurs et une croissance exponentielle des options uniques des applications.

Les fonctionnalités d'Okta comprennent, entre autres, le provisionnement, l'authentification unique (SSO), l'intégration d'Active Directory (AD) et LDAP, le déprovisionnement centralisé des utilisateurs, l'authentification multifactorielle (MFA) et des politiques flexibles pour la sécurité et le contrôle de l'organisation.



Toutes ces fonctions sont réunies dans un réseau d'applications pré-intégrées appelé {{% button href="https://www.okta.com/integrations/" %}}Okta Integration Network (OIN){{% /button %}}. L'OIN offre diverses options d'intégration, permettant une connexion SSO pour chaque application à laquelle vos utilisateurs doivent accéder pendant leur journée de travail.

Afin de permettre aux clients et aux partenaires de répondre à tous les cas d'utilisation de l'identité, nous avons construit un ensemble de composants modulaires, appelés "Platform Services", qui peuvent être combinés pour créer plus rapidement de nouvelles fonctionnalités et des expériences sur mesure. Ces Platform Services sont disponibles dans les produits packagés, les API et les SDK d'Okta.

Avantages des Platform Services Okta
- Construisez plus rapidement : mettez en place de nouvelles fonctionnalités pour couvrir plus de cas d'utilisation plus rapidement en combinant des composants préfabriqués.
- Personnalisez plus facilement : adaptez Okta à votre entreprise en utilisant des options no-code, low-code ou pro-code.
- Étendez vos services à l'ensemble de votre parc technologique : connectez-vous facilement à des applications et systèmes tiers pour améliorer la sécurité et l'expérience utilisateur.

![High Level Architecture](/images/4_Okta_Platform.png)

Les défaillances de l'infrastructure informatique sont inévitables, mais les services dans le cloud comme la gestion des identités et des accès sont essentiels pour votre entreprise et vos clients. Okta est conçu pour une redondance extrême avec des innovations uniques à chaque couche de la pile technologique pour garantir un service hautement résilient et disponible.

Les cellules innovantes d'Okta sont des instances autonomes de l'ensemble du service Okta avec des centaines de composants automatisés et modularisés. Chaque niveau de composants comporte des redondances matérielles réparties sur plusieurs zones de disponibilité AWS séparées géographiquement et logiquement les unes des autres. En outre, chaque cellule dispose d'une sauvegarde complète et d'une configuration matérielle dupliquée dans un centre de données AWS géographiquement séparé pour la reprise après sinistre.

La plateforme Okta est construite sur trois piliers pour protéger vos identités et vos données :

![High Level Architecture](/images/6_okta_pillars.png)
