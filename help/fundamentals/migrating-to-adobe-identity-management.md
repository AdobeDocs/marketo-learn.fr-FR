---
title: Migration vers Adobe Identity Management
description: Description à venir.
role: User
level: Beginner
hide: true
hidefromtoc: true
feature: Marketing
exl-id: 8368a148-c0c8-462f-b166-9efc412c4a0f
source-git-commit: fe760c2fc53b96d5c176de377730bce2e89dbc74
workflow-type: tm+mt
source-wordcount: '1079'
ht-degree: 0%

---

# Migration vers Adobe Identity Management

Adobe améliore la gestion de vos abonnements et utilisateurs Adobe Marketo Engage. Nous apportons une productivité accrue à vous et à votre entreprise en migrant vos abonnements de Marketo Engage et vos utilisateurs vers Adobe Admin Console.

Ce tutoriel vous permet de parcourir la migration afin de pouvoir gérer Adobe Marketo Engage avec d’autres comptes d’Adobe et produits pour vos utilisateurs dans un emplacement central. La migration est nécessaire et n’affecte pas votre workflow marketing, votre contenu, vos intégrations ou vos ressources.

## Liste de contrôle préalable à la migration pour les administrateurs de Marketo Engage {#pre-migration-checklist-for-marketo-engage-administrators}

Pour vous assurer que votre organisation peut migrer Adobe Marketo Engage vers Adobe Admin Console, nous vous recommandons de suivre la liste de contrôle ci-dessous pour gérer les modifications à venir.

### 1. Identifiez le ou les administrateurs système et discutez des actions qu’ils peuvent avoir à entreprendre. {#identify-your-system-administrators}

* Si vous ne savez pas qui sont les administrateurs système au sein de votre organisation, contactez votre équipe de compte d’Adobe ou contactez l’assistance Adobe `marketocares@marketo.com`.

* Confirmez le Adobe Admin Console (ou l’organisation d’Adobe) vers lequel vos abonnements de Marketo Engage seront migrés.  Les abonnements du Marketo Engage doivent être déployés dans la même organisation que Dynamic Chat, un outil d’automatisation des conversations natif intégré à Marketo Engage.
  `TBD LINK TO https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/understanding-marketo-subscription-and-user-migration-to-the-adobe-admin-console#subscription-migration-complete`

* Pour en savoir plus sur la communication avec vos administrateurs système, consultez la [section Exemple de courrier électronique](#announce-the-migration-timeline).

### 2. Familiarisez-vous avec les changements et les impacts de la migration vers Adobe Identity {#familiarize-yourself-with-the-changes}

Dans la vidéo ci-dessous, l’équipe de gestion des produits du Marketo Engage vous guide tout au long du parcours de migration et vous indique à quoi vous attendre.

>[!VIDEO](https://video.tv.adobe.com/v/3430920t3/?quality=12&learn=on){transcript=true}

Vous trouverez plus d’aide sur cette rubrique pour les administrateurs de Marketo Engage dans les articles d’aide suivants :

* [Liste de contrôle de configuration de l’utilisateur](https://experienceleague.adobe.com/en/docs/marketo/using/getting-started/initial-setup/user-setup){target="_blank"}

* [ ](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/adobe-identity-management-overview){target="_blank"} Adobe l’aperçu d’Identity Management

* [Comprendre l’abonnement Marketo et la migration des utilisateurs vers Adobe Admin Console](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/understanding-marketo-subscription-and-user-migration-to-the-adobe-admin-console){target="_blank"}

* [Migration vers Adobe Identity avec la console de migration](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/migrating-to-adobe-identity){target="_blank"}

* [Comprendre comment utiliser Adobe Admin Console](https://helpx.adobe.com/fr/enterprise/using/admin-console.html){target="_blank"}

### 3. Annoncez le calendrier et la préparation de la migration nécessaires à vos équipes internes. {#announce-the-migration-timeline}

* Marquez la date de migration sur les calendriers des administrateurs et des utilisateurs de vos Marketo Engage une fois la planification effectuée.

Vous pouvez modifier la date de migration dans **Admin** > **Console de migration** > **Prémigration** pour une meilleure alignement avec votre chronologie interne. En savoir plus sur la replanification et les limites de la [modification de la date de migration](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/migrating-to-adobe-identity#pre-migration){target="_blank"}.

* Envoyez un e-mail pour communiquer avec les administrateurs système.

Vous trouverez ci-dessous un exemple de courrier électronique que vous pouvez envoyer aux administrateurs système. En règle générale, votre service informatique gère toutes vos licences d’Adobe.

`---------------------------------------------------`

**Objet : assistance nécessaire—Migration des abonnements des Marketo Engage vers Adobe Admin Console**

Cher `[IT Administrator/NAME]`,

Notre abonnement Marketo Engage sera bientôt migré vers le système Identity Management Adobe. L’ `[Marketing Operation team]` a besoin de votre aide pour effectuer certaines étapes requises avant le début de la migration des utilisateurs, afin de minimiser l’impact sur les utilisateurs de Marketo Engage.

`1.` Confirmez si l’organisation gère déjà d’autres produits Adobe dans Adobe Admin Console et si Marketo Engage sera migré vers la même console.

* Notez que les abonnements du Marketo Engage doivent se trouver dans la même organisation que Dynamic Chat, un outil d’automatisation des conversations natif intégré à Marketo Engage.

* Si vous avez des questions ou des questions concernant l’Admin Console auquel le Marketo Engage sera ajouté, contactez l’équipe d’assistance à l’adresse `marketocares@marketo.com` et incluez-nous dans votre communication.

`2.` Faites la recherche d’un email provenant d’un Adobe avec l’objet &quot;Action requise pour gérer l’accès des utilisateurs à Adobe Marketo Engage `[Package Tier]`&quot;. Cet e-mail a été envoyé après la configuration des licences de Marketo Engage sur notre Admin Console. Seuls les administrateurs système recevront cet email. Veuillez nous informer rapidement lorsque vous le recevrez.

* Adobe peut demander votre consentement, en tant qu’administrateur système de l’Admin Console, pour migrer automatiquement les utilisateurs vers la console existante de votre entreprise. Dans l’e-mail avec l’objet &quot;Action requise pour gérer l’accès des utilisateurs à Adobe Marketo Engage `[Package Tier]`&quot;, cliquez sur le bouton &quot;Commencer&quot; pour accéder à la page de consentement.

`3.` **Facultatif :** Configuration de l’authentification unique sur Adobe Admin Console.

* Afin de permettre à nos utilisateurs de se connecter avec SSO sur leur identité d’Adobe, nous vous demandons de bien vouloir vous aider à configurer l’authentification unique sur Adobe Admin Console avant que la migration des utilisateurs ne se produise.
Nous vous sommes reconnaissants pour votre coopération durant cette transition. Dites-moi quand vous avez terminé ces étapes afin de pouvoir procéder à la migration des utilisateurs avec Marketo Engage.
Cordialement,

`[Your Name]`

`---------------------------------------------------`

* Envoyez un e-mail aux utilisateurs Marketo Engage.

Vous trouverez ci-dessous un exemple de courrier électronique que vous pouvez utiliser pour annoncer la migration à venir vers vos utilisateurs Marketo Engage qui ne disposent pas des privilèges d’administrateur.

`---------------------------------------------------`

**Objet : mise à jour importante—Migration des abonnements de Marketo Engage vers Adobe Admin Console**

Chers utilisateurs Marketo Engage,

Nous avons une annonce importante concernant notre instance de Marketo Engage et la manière dont vous vous connecterez. Adobe déplace les abonnements et les utilisateurs des Marketo Engage vers Adobe Admin Console afin de permettre à leurs clients de centraliser toute l’administration de leurs produits au même endroit. Cela n’aura aucune incidence sur les workflows marketing, le contenu, les intégrations ou les ressources.

Détails clés :

* Date de migration : [Spécifiez la date planifiée - veuillez la trouver en Marketo Engage sous **Admin** > **Console de migration** > **Avant-migration**]

* Minutage : la migration commence vers minuit, heure locale, pour notre abonnement.

* Impact : il n’y aura aucune perte d’accès aux produits lors de la migration des utilisateurs. Si vous êtes connecté lors de la migration de votre compte, vous serez déconnecté et invité à vous reconnecter dans les minutes qui suivent la migration à l’aide de Adobe Identity.

* Avantages : authentifiez le Marketo Engage et d’autres produits Adobe en utilisant une seule identité d’Adobe, qu’il s’agisse d’un Adobe ID ou d’un Federated ID d’Adobe (SSO).

Ce que vous devez faire :

`1.` Préparer : la vérification des emails est nécessaire pour que vous puissiez être migré vers une identité d’Adobe.

i. Vous avez reçu un courrier électronique de demande de vérification de l’email contenant un lien (reste valide pendant 3 jours). Si votre lien a expiré, vous pouvez renvoyer l’e-mail de vérification en accédant à **Admin** > **Mon compte** > **Paramètres du compte** et en cliquant sur **Renvoyer la vérification**.
ii. Une session d’utilisateur active est requise pour le succès de la vérification des emails. Connectez-vous à votre abonnement de Marketo Engage à l’aide de l’URL de votre fournisseur d’identité (IdP).

`2.` Onboard : une fois votre compte utilisateur migré, vous recevrez un e-mail de l’Adobe concernant les modifications apportées à votre méthode de connexion.

i. Acceptez la nouvelle invitation en cliquant sur le bouton &quot;Accepter l’invitation&quot; et en vous connectant à l’aide de Adobe Identity.
ii. Sur la page de connexion de l’Adobe, connectez-vous avec un Adobe ID existant.

`3.` Contact : si vous avez des questions ou avez besoin d’aide après la migration de votre compte ou si votre compte n’est pas migré et que vous avez perdu l’accès à Marketo Engage, contactez l’équipe de migration de Marketo Engage à l’adresse `[your internal contact email/phone]`.

Nous vous sommes reconnaissants pour votre coopération durant cette transition. Merci pour votre compréhension et votre engagement à préserver la sécurité de nos systèmes.

Cordialement,

`[Your Name]`

`---------------------------------------------------`
