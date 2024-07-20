---
title: Développement d’un guide de gouvernance d’instance avec de la documentation
description: Découvrez comment établir une procédure robuste pour créer et gérer la documentation et le fichier de modification pour votre instance de Marketo Engage. Cela permet non seulement de gagner du temps pour le partage des connaissances de votre équipe, mais également d’améliorer la santé et l’efficacité de votre instance.
feature: Administration
role: Admin
level: Intermediate, Experienced
doc-type: Tutorial
last-substantial-update: 2023-10-16T00:00:00Z
jira: KT-14103
thumbnail: KT-14103.jpeg
hide: false
exl-id: 4313b54a-1848-4684-b037-7a7795dd01ec
source-git-commit: 681d390ce5ab336a7e24cc63256659a492288517
workflow-type: tm+mt
source-wordcount: '896'
ht-degree: 1%

---

# Développement d’un guide de gouvernance d’instance avec de la documentation

Lorsque vous entrez dans une instance [!DNL Marketo Engage] héritée, il s’agit souvent de manquer de documentation fonctionnelle et technique à jour. En tant qu’administrateur, l’établissement de directives pour garantir une gouvernance d’instance appropriée est une responsabilité essentielle que vous ne pouvez pas négliger. Il s’agit de l’une des stratégies critiques pour [stimuler l’efficacité pendant que vous travaillez dans une instance de Marketo Engage établie](https://nation.marketo.com/t5/champion-program-blogs/3-tips-to-increase-your-efficiency-in-an-inherited-instance/ba-p/247582).

Ce tutoriel détaillé provenant de [!DNL Adobe Marketo Champion] (2018), Nick Hajdin, vous guidera tout au long de ce processus pour décrire la configuration de votre instance, documenter vos programmes opérationnels principaux et gérer un [!DNL changelog] pour appliquer une politique de gouvernance stricte.

## Pourquoi développer un guide et une documentation de gouvernance d’instance pour votre instance héritée ?

Une documentation détaillée et un [!DNL changelog] sont essentiels pour une gestion efficace et un transfert de connaissances au sein de votre instance [!DNL Marketo Engage]. Le suivi des modifications et des décisions que vous avez apportées lors de la configuration de votre instance peut vous aider à :

1. Entraînez plus facilement les utilisateurs internes de manière évolutive.
2. Créez plus efficacement dans [!DNL Marketo Engage] à long terme.
3. Maintenez l’intégrité et l’hygiène de votre instance à l’avenir afin de vous éviter de passer des heures à fouiller dans les emails, le [journal d’audit](https://experienceleague.adobe.com/docs/marketo/using/product-docs/administration/audit-trail/audit-trail-overview.html) et le [journal d’activité](https://experienceleague.adobe.com/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/managing-people-in-smart-lists/locate-the-activity-log-for-a-person.html) pour obtenir un contexte.
4. Gagnez du temps lors du transfert de [!DNL Marketo Engage] connaissances à un nouvel administrateur [!DNL Marketo Engage] si votre équipe connaît un quelconque chiffre d&#39;affaires.

## [!DNL Marketo Engage] Guide de gouvernance 101

Un guide de gouvernance sert de source de vérité pour la configuration de l’instance et les exigences de conception du système. Les informations clés recommandées à inclure dans ce document sont les suivantes :

* Structures de programme/dossier
* Autorisation utilisateur et rôle
* Limites de communication
* Normes de gouvernance
* Formation des utilisateurs internes avant de leur accorder l’accès à la plateforme

## Comment développer et gérer un guide de gouvernance pour votre instance [!DNL Marketo Engage]

### Étape 1 : Identifiez votre guide et votre documentation actuels sur l’état de gouvernance

* **Je ne parviens pas à trouver de documentation pour mon instance héritée :** Si vous avez récemment démarré un nouveau rôle et que vous ne parvenez pas à localiser la documentation de votre instance héritée, **passez à l’étape 2** et commencez avec un modèle téléchargeable que nous avons fourni.
* **J&#39;ai de la documentation sur le fichier :** Félicitations, c&#39;est un bon signe ! Veillez à vérifier leur pertinence pour savoir quand la dernière modification est effectuée. S’il n’est pas activement géré par les membres de votre équipe, il est recommandé de les actualiser et d’informer vos utilisateurs internes sur la manière de le tenir à jour.

### Étape 2 : Identifiez les éléments à inclure dans votre [!DNL Marketo Engage] Documentation &amp; [!DNL Changelogs]

Le format varie d’une plateforme basée sur le cloud à un document partagé. Vous pouvez concevoir le format qui répond aux besoins de votre entreprise. [Voici une documentation simple et un modèle Excel changelog](/help/tutorial-inherited-instance/_assets/downloads/Adobe_Marketo_Engage_Inherited_Instance_Documentation-Changlog.xlsx) qui couvre les éléments importants que vous pouvez commencer à utiliser. Voici quelques-unes de ces fonctions :

* Documentation
   * Nom du modèle de programme
   * Canal
   * Date de création
   * Créé par
   * Objectif du programme
   * Statut
   * Lien vers le modèle de programme
   * Note
* Changelog
   * Nom du modèle de programme
   * Date de changement
   * Mis à jour par
   * Objectif de la mise à jour
   * Expérience avant modification (inclure des liens/captures d’écran)
   * Expérience après modification (inclure des liens/captures d’écran)
   * URL du programme

### Étape 3 : identifier et documenter l&#39;état actuel des programmes opérationnels principaux

Commencez par identifier les programmes opérationnels clés ayant un impact au niveau de l’abonnement. Par exemple, les campagnes de Data Management, le cycle de vie des prospects, la notation des prospects, la synchronisation [!DNL CRM] et la délivrabilité.

Pour chaque programme opérationnel identifié, documentez son état actuel. Cela inclut des détails sur l’objectif du programme, la configuration, les campagnes intelligentes associées et l’intégration à d’autres outils (le cas échéant).

### Étape 4 : Application de la maintenance [!DNL Changelog]

L’étape suivante consiste à établir une stratégie de gouvernance stricte pour votre instance [!DNL Marketo Engage] qui requiert la &quot;[!DNL Changelog] maintenance&quot;. Cette politique garantit que toutes les mises à jour apportées aux programmes opérationnels dans l’instance sont entièrement documentées.

Eduquez votre équipe sur l&#39;importance de ces documents et comment y accéder et les mettre à jour correctement. Il peut s’avérer utile d’attribuer des responsabilités pour la gestion du journal des modifications. Ainsi, quelques membres ou administrateurs désignés de l’équipe des opérations marketing enregistrent régulièrement les modifications et fournissent des signatures.

### Étape 5 : Centralisation de la documentation

Créez un emplacement central ou un référentiel pour stocker toute la documentation relative à votre instance [!DNL Marketo Engage]. Il peut s’agir d’un lecteur partagé, d’un dossier dédié ou d’un système basé sur le cloud.

### Étape 6 : Révision et mise à jour régulières

Planifiez des révisions régulières de votre documentation afin de vous assurer qu’elle reste exacte et à jour. On peut facilement l&#39;ignorer pendant les heures de pointe. Configurez de manière proactive des rappels sur votre calendrier afin de vous assurer que votre équipe effectue régulièrement des mises à jour pour refléter les modifications ou les optimisations de vos programmes opérationnels.

## Et après ?

Commencez en téléchargeant ce [modèle simple](/help/tutorial-inherited-instance/_assets/downloads/Adobe_Marketo_Engage_Inherited_Instance_Documentation-Changlog.xlsx).

Suivez les étapes ci-dessus pour développer votre guide de gouvernance et votre documentation. Pendant que vous effectuez le processus, tenez compte des règles de base suivantes :

**Mettez à jour votre documentation existante :**
Il est essentiel de garder votre documentation à jour. S’il n’a pas été modifié depuis 3 ans, prenez le temps de réviser votre documentation au fur et à mesure que vous contrôlez votre instance.

**Partager et entraîner :**
Partagez votre documentation et [!DNL changelog] avec les membres de l&#39;équipe concernés et apprenez-les à mettre à jour ces enregistrements.

**Révision périodique :** programmez le temps de les passer en revue et de les gérer tout au long de l’année pour inclure de nouveaux changements, optimisations ou ajustements au fur et à mesure qu’ils se produisent.

La maintenance d’une documentation complète et à jour pour votre instance de Marketo Engage vous fera gagner du temps et vous fera gagner du temps et vous aidera à gérer efficacement les instances.

### Auteurs

**Nick Hajdin**
[!DNL Adobe Marketo Champion] (2018)
*[!DNL Digital Technology Senior Manager at Accenture]*

![Nick Hajdin](/help/tutorial-inherited-instance/_assets/authors/Customer_Author_Nicholas_Hajdin.png){width="30%"}

**Amy Chiu**
*Gestionnaire marketing d’adoption et de rétention, Adobe*

![Amy Chiu](/help/tutorial-inherited-instance/_assets/authors/Adobe_Author_Amy_Chiu.png){width=30%}
