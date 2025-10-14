---
title: Migration vers Adobe Identity Management
description: Ce tutoriel vous aidera à naviguer dans la migration de vos abonnements et utilisateurs Marketo Engage vers Adobe Admin Console.
role: Admin
level: Intermediate, Experienced
recommendations: noDisplay, noCatalog
last-substantial-update: 2024-07-26T00:00:00Z
feature: Marketing
exl-id: 8368a148-c0c8-462f-b166-9efc412c4a0f
source-git-commit: dcfffa299cbcfef489f5b618fae29f745b878d26
workflow-type: tm+mt
source-wordcount: '1250'
ht-degree: 0%

---

# Migration vers Adobe Identity Management

Adobe améliore la gestion de vos abonnements et de vos utilisateurs Adobe Marketo Engage. Nous augmentons la productivité de votre entreprise en migrant vos abonnements et vos utilisateurs Marketo Engage vers Adobe Admin Console.

Ce tutoriel vous aidera à parcourir la migration afin de commencer à gérer Adobe Marketo Engage avec d’autres comptes et produits Adobe pour vos utilisateurs à un emplacement centralisé. La migration est nécessaire et n’affecte pas votre workflow marketing, votre contenu, vos intégrations ou vos ressources.

## Liste de contrôle de pré-migration pour les administrateurs Marketo Engage {#pre-migration-checklist-for-marketo-engage-administrators}

Pour que votre entreprise puisse migrer Adobe Marketo Engage vers Adobe Admin Console, nous vous recommandons de suivre la liste de contrôle ci-dessous pour gérer les modifications à venir.

### 1. Identifiez votre ou vos administrateur(s) système(s) et votre équipe informatique et discutez des actions qu’ils peuvent devoir entreprendre {#identify-your-system-administrators}

* Si vous ne savez pas qui sont les administrateurs système au sein de votre organisation, contactez l’équipe chargée de votre compte Adobe Adobe ou contactez l’assistance technique d’`marketocares@marketo.com`.

* Confirmez le Adobe Admin Console (ou l’organisation Adobe) vers lequel votre ou vos abonnements Marketo Engage seront migrés. Vous disposez probablement d’un Adobe Admin Console pour [Dynamic Chat](/help/dynamic-chat/dynamic-chat-overview.md){target="_blank"}, un outil d’automatisation des conversations natif dans Marketo Engage. Le ou les abonnements Marketo Engage doivent être déployés dans la même organisation que Dynamic Chat.

* Collaborez avec votre équipe informatique pour placer sur la liste autorisée tous les domaines Adobe répertoriés [au début de cet article](https://experienceleague.adobe.com/fr/docs/marketo/using/getting-started/initial-setup/configure-protocols-for-marketo){target="_blank"} afin d’éviter toute perturbation de l’accès à Marketo Engage après la migration vers Adobe Identity.

* **Facultatif :** [&#x200B; Implémenter l’authentification unique (SSO)](https://experienceleague.adobe.com/fr/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/understanding-marketo-subscription-and-user-migration-to-the-adobe-admin-console#subscription-migration-complete){target="_blank"} avant la migration des utilisateurs.

  >[!NOTE]
  >
  >Il existe des différences entre la connexion unique prise en charge par Marketo Engage et la connexion unique Adobe Admin Console. Par conséquent, il se peut que des modifications apportées à votre configuration doivent être implémentées.

* **Facultatif :** personnalisez la [durée de vie de session maximale souhaitée](https://helpx.adobe.com/fr/enterprise/using/authentication-settings.html#advanced-settings){target="_blank"} avant la migration des utilisateurs pour que les utilisateurs de Marketo Engage restent authentifiés.

* Découvrez les éléments à communiquer avec vos administrateurs système dans la [section Exemple d’e-mail](#announce-the-migration-timeline).

### 2. Familiarisez-vous avec les changements et les impacts de la migration vers Adobe Identity {#familiarize-yourself-with-the-changes}

Dans la vidéo ci-dessous, l’équipe de gestion des produits Marketo Engage vous guide tout au long du parcours de migration et vous explique ce à quoi vous attendre.

>[!VIDEO](https://video.tv.adobe.com/v/3432365/?t=170/?quality=12&learn=on&captions=fre_fr){transcript=true}

Vous trouverez plus d’informations sur cette rubrique pour les administrateurs de Marketo Engage dans les articles d’aide suivants :

* [Liste de contrôle relative à la configuration utilisateur](https://experienceleague.adobe.com/fr/docs/marketo/using/getting-started/initial-setup/user-setup){target="_blank"}

* [Présentation d’Adobe Identity Management](https://experienceleague.adobe.com/fr/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/adobe-identity-management-overview){target="_blank"}

* [Présentation de l’abonnement à Marketo et de la migration des utilisateurs vers Adobe Admin Console](https://experienceleague.adobe.com/fr/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/understanding-marketo-subscription-and-user-migration-to-the-adobe-admin-console){target="_blank"}

* [Migration vers Adobe Identity avec la console de migration](https://experienceleague.adobe.com/fr/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/migrating-to-adobe-identity){target="_blank"}

* [Comprendre comment utiliser Adobe Admin Console](https://helpx.adobe.com/fr/enterprise/using/admin-console.html){target="_blank"}

### 3. Annoncez le calendrier de migration et la préparation nécessaire à vos équipes internes {#announce-the-migration-timeline}

* Marquez la date de migration sur les calendriers de vos administrateurs et utilisateurs Marketo Engage une fois planifiée.

   * Vous pouvez modifier la date de migration dans **Admin** > **Console de migration** > **Pré-migration** pour mieux l’adapter à votre calendrier interne. En savoir plus sur la replanification et les limites de la [modification de la date de migration](https://experienceleague.adobe.com/fr/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/migrating-to-adobe-identity#pre-migration){target="_blank"}.

* **Envoyer un e-mail aux administrateurs système**

Vous trouverez ci-dessous un exemple d’e-mail à envoyer à vos administrateurs. En règle générale, votre service informatique gère toutes vos licences Adobe.

+++ Exemple d’e-mail à envoyer à vos administrateurs système

**Objet : Assistance requise — Migration des abonnements Marketo Engage vers Adobe Admin Console**

Cher `[IT Administrator/NAME]`,

Notre abonnement Marketo Engage sera bientôt migré vers le système Adobe Identity Management. Le `[Marketing Operation team]` a besoin de votre aide pour effectuer certaines étapes nécessaires avant le début de la migration des utilisateurs, afin de minimiser l’impact sur les utilisateurs de Marketo Engage.

`1.` Confirmez si l’entreprise gère déjà d’autres produits Adobe dans Adobe Admin Console et si Marketo Engage sera migré vers la même console.

* Le ou les abonnements Marketo Engage doivent se trouver dans la même organisation que Dynamic Chat, un outil d’automatisation des conversations natif intégré à Marketo Engage.

* Si vous avez des questions ou des préoccupations concernant Admin Console, contactez l’assistance Adobe à l’adresse `marketocares@marketo.com` et CC us.

`2.` être à l’affût d’un e-mail d’Adobe avec pour objet « Action requise pour gérer l’accès des utilisateurs et utilisatrices aux `[Package Tier]` Adobe Marketo Engage ». Cet e-mail a été envoyé après la configuration des licences Marketo Engage sur notre Admin Console. Seuls les administrateurs système recevront cet e-mail. Merci de nous informer rapidement lorsque vous le recevrez.

* Adobe peut demander votre consentement, en tant qu’administrateur système d’Admin Console, pour migrer automatiquement les utilisateurs vers la console existante de votre entreprise. Dans l’e-mail avec pour objet « Action requise pour gérer l’accès des utilisateurs et utilisatrices à Adobe Marketo Engage `[Package Tier]` », cliquez sur le bouton « Commencer » pour accéder à la page de consentement.

`3.` Après la migration, Marketo Engage ne sera plus diffusée depuis experience.adobe.com vers Adobe Experience Cloud. Placer sur la liste autorisée Veuillez tous les domaines Adobe répertoriés [en haut de cet article](https://experienceleague.adobe.com/fr/docs/marketo/using/getting-started/initial-setup/configure-protocols-for-marketo){target="_blank"} pour éviter toute interruption de notre accès à Marketo Engage.

`4.` **Facultatif :** configurez l’authentification unique (SSO) dans Adobe Admin Console.

* À l’avenir, pour les utilisateurs qui se connectent avec l’authentification unique sur leur identité Adobe, vous devrez aider à la configuration de l’authentification unique dans le Adobe Admin Console avant la migration des utilisateurs.

`5.` **Facultatif :** définissez une durée de vie de session [maximale](https://helpx.adobe.com/fr/enterprise/using/authentication-settings.html#advanced-settings){target="_blank"} plus longue dans le Adobe Admin Console.

* Pour éviter aux utilisateurs d’avoir à se connecter fréquemment, personnalisez la durée de vie de la session dans les Paramètres avancés sur une durée plus longue.

Nous apprécions votre coopération durant cette transition. Prévenez-moi lorsque vous avez terminé ces étapes afin que je puisse procéder à la migration.

Cordialement,

`[Your Name]`

+++

* **Envoyer un e-mail aux utilisateurs de Marketo Engage**

Vous trouverez ci-dessous un exemple d’e-mail pour les utilisateurs de Marketo Engage qui ne disposent **pas** de privilèges d’administrateur.

+++ Exemple d’e-mail annonçant la migration à venir

**Objet : Mise à jour importante—Migration des abonnements Marketo Engage vers Adobe Admin Console**

Chers utilisateurs de Marketo Engage,

Nous avons une annonce importante concernant notre instance Marketo Engage et la manière dont vous vous connecterez. Adobe déplace les abonnements Marketo Engage et les utilisateurs vers Adobe Admin Console afin de nous permettre de centraliser toute l’administration de leurs produits dans un seul emplacement. Cela n’affecte pas les workflows marketing, le contenu, les intégrations ou les ressources.

**Détails clés :**

* **Date de migration** : `[Specify the scheduled date - please find this in Marketo Engage under Admin > Migration Console > Pre-migration]`

* **Timing** : la migration commence vers minuit heure locale pour notre abonnement.

* **Impact** : il n’y aura aucune perte d’accès au produit lors de la migration des utilisateurs. Si vous êtes connecté lors de la migration de votre compte, vous serez déconnecté et invité à vous reconnecter dans les minutes qui suivent l’utilisation d’Adobe Identity après la migration.

* **Avantages** : authentifiez Marketo Engage et d’autres produits Adobe à l’aide d’une seule identité Adobe, à savoir une Adobe ID ou un Adobe Federated ID (SSO).

**Ce que vous devez faire**

`1.` **Préparer** : la vérification des e-mails est nécessaire pour que vous puissiez migrer vers une identité Adobe.

i. Vous avez reçu un e-mail de demande de vérification par e-mail contenant un lien (valable 3 jours). Si votre lien a expiré, vous pouvez renvoyer l’e-mail de vérification depuis Marketo Engage en cliquant sur l’icône « Mon profil », puis en accédant à **Mon compte** > **Paramètres du compte** > **Renvoyer la vérification**.

ii. Une session utilisateur active est requise pour que la vérification des e-mails réussisse. Veuillez d’abord vous connecter à votre abonnement Marketo Engage à l’aide de l’URL de votre fournisseur d’identité (IdP).

`2.` **Intégration** : une fois votre compte utilisateur migré, vous recevrez un e-mail d’Adobe concernant les modifications apportées à votre méthode de connexion.

i. Acceptez la nouvelle invitation en cliquant sur le bouton « Accepter l’invitation » et en vous connectant à l’aide d’Adobe Identity.

ii. Sur la page de connexion d’Adobe, connectez-vous avec un Adobe ID existant.

iii. Vous devez d’abord vous connecter à l’instance Marketo Engage pour toute URL précédemment marquée d’un signet sur le domaine engage-xx.marketo.com vers lequel vous naviguez.

`3.` **Contact** : si vous avez des questions ou si vous avez besoin d’aide après la migration de votre compte, ou si votre compte n’a pas été migré et que vous avez perdu l’accès à Marketo Engage, veuillez contacter l’équipe de migration de Marketo Engage à l’adresse `[your internal contact email/phone]`.

Nous apprécions votre coopération durant cette transition. Merci de votre compréhension et de votre engagement à assurer la sécurité de nos systèmes.

Cordialement,

`[Your Name]`

+++
