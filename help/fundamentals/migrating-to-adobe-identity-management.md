---
title: Migration vers Adobe Identity Management
description: Ce tutoriel vous aidera à naviguer dans la migration de vos abonnements et utilisateurs et utilisatrices Marketo Engage vers Adobe Admin Console.
role: Admin
level: Intermediate, Experienced
recommendations: noDisplay, noCatalog
last-substantial-update: 2024-07-26T00:00:00Z
feature: Marketing
exl-id: 8368a148-c0c8-462f-b166-9efc412c4a0f
source-git-commit: dcfffa299cbcfef489f5b618fae29f745b878d26
workflow-type: ht
source-wordcount: '1250'
ht-degree: 100%

---

# Migration vers Adobe Identity Management

Adobe améliore la gestion de vos abonnements et de vos utilisateurs et utilisatrices Adobe Marketo Engage. Nous augmentons la productivité de votre entreprise en migrant vos abonnements et vos utilisateurs et utilisatrices Marketo Engage vers Adobe Admin Console.

Ce tutoriel vous aidera à parcourir la migration afin de commencer à gérer Adobe Marketo Engage avec d’autres comptes et produits Adobe pour vos utilisateurs et utilisatrices à un emplacement centralisé. La migration est nécessaire et n’affecte pas votre workflow marketing, votre contenu, vos intégrations ou vos ressources.

## Liste de contrôle pré-migration pour les administrateurs et administratrices Marketo Engage {#pre-migration-checklist-for-marketo-engage-administrators}

Pour que votre entreprise puisse migrer Adobe Marketo Engage vers Adobe Admin Console, nous vous recommandons de suivre la liste de contrôle ci-dessous pour gérer les modifications à venir.

### &#x200B;1. Identifier vos équipes d’administration système et informatique et discuter des actions potentiellement à entreprendre {#identify-your-system-administrators}

* Si vous ne savez pas qui sont les administrateurs et administratrices système au sein de votre organisation, contactez l’équipe Adobe en charge des comptes ou contactez l’assistance technique Adobe `marketocares@marketo.com`.

* Confirmez l’Adobe Admin Console (ou l’organisation Adobe) vers laquelle votre ou vos abonnements Marketo Engage seront migrés. Vous disposez probablement d’une Adobe Admin Console pour [Dynamic Chat](/help/dynamic-chat/dynamic-chat-overview.md){target="_blank"}, un outil d’automatisation des conversations natif dans Marketo Engage. Le ou les abonnements Marketo Engage doivent être déployés dans la même organisation que Dynamic Chat.

* Collaborez avec votre équipe informatique pour placer sur la liste autorisée tous les domaines Adobe répertoriés [au début de cet article](https://experienceleague.adobe.com/fr/docs/marketo/using/getting-started/initial-setup/configure-protocols-for-marketo){target="_blank"} afin d’éviter toute perturbation de l’accès à Marketo Engage après la migration vers Adobe Identity.

* **Facultatif :** [implémentez l’authentification unique (SSO)](https://experienceleague.adobe.com/fr/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/understanding-marketo-subscription-and-user-migration-to-the-adobe-admin-console#subscription-migration-complete){target="_blank"} avant la migration des utilisateurs et utilisatrices.

  >[!NOTE]
  >
  >Il existe des différences entre l’authentification unique prise en charge par Marketo Engage et l’authentfication unique Adobe Admin Console. Par conséquent, il se peut que des modifications apportées à votre configuration doivent être implémentées.

* **Facultatif :** personnalisez la [durée de vie de session maximale souhaitée](https://helpx.adobe.com/enterprise/using/authentication-settings.html#advanced-setting){target="_blank"} avant la migration des utilisateurs et utilisatrices pour que les utilisateurs et utilisatrices de Marketo Engage restent authentifiés.

* Découvrez les éléments à communiquer avec vos administrateurs et administratrices système dans la [section Exemple d’e-mail](#announce-the-migration-timeline).

### &#x200B;2. Se familiariser avec les changements et les impacts de la migration vers Adobe Identity {#familiarize-yourself-with-the-changes}

Dans la vidéo ci-dessous, l’équipe de gestion des produits Marketo Engage vous guide tout au long du parcours de migration et vous explique ce à quoi vous attendre.

>[!VIDEO](https://video.tv.adobe.com/v/3430920t3/?t=170/?quality=12&learn=on){transcript=true}

Vous trouverez plus d’informations sur cette rubrique pour les administrateurs et administratrices de Marketo Engage dans les articles d’aide suivants :

* [Liste de contrôle relative à la configuration des utilisateurs et utilisatrices](https://experienceleague.adobe.com/fr/docs/marketo/using/getting-started/initial-setup/user-setup){target="_blank"}

* [Vue d’ensemble d’Adobe Identity Management](https://experienceleague.adobe.com/fr/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/adobe-identity-management-overview){target="_blank"}

* [Présentation de l’abonnement à Marketo et de la migration des utilisateurs et utilisatrices vers Adobe Admin Console](https://experienceleague.adobe.com/fr/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/understanding-marketo-subscription-and-user-migration-to-the-adobe-admin-console){target="_blank"}

* [Migration vers Adobe Identity avec la console de migration](https://experienceleague.adobe.com/fr/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/migrating-to-adobe-identity){target="_blank"}

* [Découvrir comment utiliser Adobe Admin Console](https://helpx.adobe.com/fr/enterprise/using/admin-console.html){target="_blank"}

### &#x200B;3. Annoncer la chronologie de migration et la préparation nécessaire à vos équipes internes {#announce-the-migration-timeline}

* Une fois la migration planifiée, marquez la date de migration sur les calendriers de vos administrateurs et administratrices et utilisateurs et utilisatrices Marketo Engage.

   * Vous pouvez modifier la date de migration dans **Admin** > **Console de migration** > **Pré-migration** pour mieux l’adapter à votre chronologie interne. En savoir plus sur la replanification et les limites de la [modification de la date de migration](https://experienceleague.adobe.com/fr/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/migrating-to-adobe-identity#pre-migration){target="_blank"}.

* **Envoyer un e-mail aux administrateurs et administratrices système**

Vous trouverez ci-dessous un exemple d’e-mail à envoyer à vos administrateurs et administratrices. En règle générale, votre service informatique gère toutes vos licences Adobe.

+++ Exemple d’e-mail à envoyer à vos administrateurs et administratrices système

**Objet : Assistance requise : migration des abonnements Marketo Engage vers Adobe Admin Console**

Bonjour `[IT Administrator/NAME]`,

Notre abonnement Marketo Engage subira bientôt une migration vers le système Adobe Identity Management. L’`[Marketing Operation team]` a besoin de votre aide pour effectuer certaines étapes nécessaires avant le début de la migration des utilisateurs et utilisatrices de Marketo Engage afin de minimiser l’impact sur ces derniers.

`1.` Confirmez si l’entreprise gère déjà d’autres produits Adobe dans Adobe Admin Console et si Marketo Engage fera l’objet d’une migration vers la même console.

* Le ou les abonnements Marketo Engage doivent se trouver dans la même organisation que Dynamic Chat, un outil d’automatisation des conversations natif intégré à Marketo Engage.

* Si vous avez des questions ou des préoccupations concernant Admin Console, contactez l’assistance Adobe à l’adresse `marketocares@marketo.com` et mettez-nous en copie de l’e-mail.

`2.` Surveillez la réception d’un e-mail d’Adobe avec pour objet « Action requise pour gérer l’accès des utilisateurs et utilisatrices à Adobe Marketo Engage `[Package Tier]` ». Cet e-mail a été envoyé après la configuration des licences Marketo Engage sur notre Admin Console. Seuls les administrateurs et administratrices système recevront cet e-mail. Merci de nous informer rapidement lorsque vous le recevez.

* Adobe peut demander votre consentement, en tant qu’administrateur ou administratrice système d’Admin Console, pour migrer automatiquement les utilisateurs et utilisatrices vers la console existante de votre entreprise. Dans l’e-mail avec pour objet « Action requise pour gérer l’accès des utilisateurs et utilisatrices à Adobe Marketo Engage `[Package Tier]` », cliquez sur le bouton « Commencer » pour accéder à la page de consentement.

`3.` Après la migration, le service de Marketo Engage passera de experience.adobe.com à Adobe Experience Cloud. Veuillez placer sur la liste autorisée tous les domaines Adobe répertoriés [en haut de cet article](https://experienceleague.adobe.com/fr/docs/marketo/using/getting-started/initial-setup/configure-protocols-for-marketo){target="_blank"} pour éviter toute interruption de notre accès à Marketo Engage.

`4.` **Facultatif :** configurez l’authentification unique (SSO) dans Adobe Admin Console.

* À l’avenir, pour les utilisateurs et utilisatrices qui se connectent avec l’authentification unique sur leur identité Adobe, vous devrez aider à la configuration de l’authentification unique dans Adobe Admin Console avant leur migration.

`5.` **Facultatif :** définissez une [durée de vie de session maximale](https://helpx.adobe.com/enterprise/using/authentication-settings.html#advanced-setting){target="_blank"} plus longue dans Adobe Admin Console.

* Pour éviter aux utilisateurs et utilisatrices d’avoir à se connecter fréquemment, personnalisez la durée de vie de la session dans les Paramètres avancés avec une durée plus longue.

Nous apprécions votre coopération durant cette transition. Prévenez-moi lorsque vous avez terminé ces étapes afin que je puisse procéder à la migration.

Cordialement,

`[Your Name]`

+++

* **Envoyer un e-mail aux utilisateurs et utilisatrices de Marketo Engage**

Vous trouverez ci-dessous un exemple d’e-mail pour les utilisateurs et utilisatrices de Marketo Engage qui ne disposent **pas** de privilèges d’administration.

+++ Exemple d’e-mail annonçant la migration à venir

**Objet : Mise à jour importante : migration des abonnements Marketo Engage vers Adobe Admin Console**

Chers utilisateurs et utilisatrices d’Adobe Marketo Engage,

Nous avons une annonce importante concernant notre instance Marketo Engage et la manière dont vous vous connecterez. Adobe déplace les abonnements Marketo Engage ainsi que ses utilisateurs et utilisatrices vers Adobe Admin Console afin de nous permettre de centraliser toute l’administration de leurs produits dans un seul emplacement. Cela n’affecte pas les workflows marketing, le contenu, les intégrations ou les ressources.

**Détails clés :**

* **Date de migration** : `[Specify the scheduled date - please find this in Marketo Engage under Admin > Migration Console > Pre-migration]`

* **Timing** : la migration commence vers minuit heure locale pour notre abonnement.

* **Impact** : aucune perte d’accès au produit ne se produira lors de la migration des utilisateurs et utilisatrices. Si votre connexion est effective lors de la migration de votre compte, vous ferez l’objet d’une déconnexion et recevrez une invitation à vous reconnecter dans les minutes qui suivent l’utilisation d’Adobe Identity après la migration.

* **Avantages** : s’authentifier auprès de Marketo Engage et d’autres produits Adobe à l’aide d’un seul identifiant Adobe, à savoir un Adobe ID ou un Adobe Federated ID (SSO).

**Ce que vous devez faire :**

`1.` **Préparation** : la vérification des e-mails est nécessaire pour que vous puissiez migrer vers une identité Adobe.

i. Vous avez reçu un e-mail de demande de vérification par e-mail contenant un lien (valable 3 jours). Si votre lien a expiré, vous pouvez renvoyer l’e-mail de vérification depuis Marketo Engage en cliquant sur l’icône « Mon profil », puis en accédant à **Mon compte** > **Paramètres du compte** > **Renvoyer la vérification**.

ii. Une session d’utilisation active est requise pour que la vérification par e-mail réussisse. Veuillez d’abord vous connecter à votre abonnement Marketo Engage à l’aide de l’URL de votre fournisseur d’identité (IdP).

`2.` **Intégration** : une fois votre compte d’utilisateur ou d’utilisatrice migré, vous recevrez un e-mail d’Adobe concernant les modifications apportées à votre méthode de connexion.

i. Acceptez la nouvelle invitation en cliquant sur le bouton « Accepter l’invitation » et en vous connectant à l’aide d’Adobe Identity.

ii. Sur la page de connexion d’Adobe, connectez-vous avec un Adobe ID existant.

iii. Vous devez d’abord vous connecter à l’instance Marketo Engage pour toute URL précédemment marquée d’un signet sur le domaine engage-xx.marketo.com vers lequel vous naviguez.

`3.` **Contact** : si vous avez des questions, si vous avez besoin d’aide après la migration de votre compte, ou si votre compte n’a pas été migré et que vous avez perdu l’accès à Marketo Engage, veuillez contacter l’équipe de migration de Marketo Engage à l’adresse `[your internal contact email/phone]`.

Nous apprécions votre coopération durant cette transition. Merci de votre compréhension et de votre engagement pour assurer la sécurité de nos systèmes.

Cordialement,

`[Your Name]`

+++
