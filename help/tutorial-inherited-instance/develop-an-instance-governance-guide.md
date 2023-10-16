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
source-git-commit: 4dc6aeed353fdd8bac960603af22b060ae2d7f00
workflow-type: tm+mt
source-wordcount: '906'
ht-degree: 1%

---


# Développement d’un guide de gouvernance d’instance avec de la documentation

Lorsque vous entrez dans un ancien [!DNL Marketo Engage] Par exemple, il s’agit souvent d’un problème de manque de documentation fonctionnelle et technique à jour. En tant qu’administrateur, l’établissement de directives pour garantir une gouvernance d’instance appropriée est une responsabilité essentielle que vous ne pouvez pas négliger. C&#39;est l&#39;une des stratégies cruciales pour [efficacité du lecteur lorsque vous travaillez sur une instance Marketo Engage établie](https://nation.marketo.com/t5/champion-program-blogs/3-tips-to-increase-your-efficiency-in-an-inherited-instance/ba-p/247582).

Ce tutoriel détaillé issu de [!DNL Adobe Marketo Champion] (2018), Nick Hajdin, vous guidera tout au long de ce processus pour décrire la configuration de votre instance, documenter vos programmes opérationnels principaux et gérer une [!DNL changelog] pour appliquer une politique de gouvernance stricte.

## Pourquoi développer un guide et une documentation de gouvernance d’instance pour votre instance héritée ?

Documentation détaillée et une [!DNL changelog] sont essentiels à une gestion efficace et au transfert des connaissances au sein de votre [!DNL Marketo Engage] instance. Le suivi des modifications et des décisions que vous avez apportées lors de la configuration de votre instance peut vous aider à :

1. Entraînez plus facilement les utilisateurs internes de manière évolutive.
2. Créez plus efficacement dans [!DNL Marketo Engage] à long terme.
3. Maintenez l&#39;intégrité et l&#39;hygiène de votre instance à l&#39;avenir pour vous éviter de passer des heures à fouiller dans les emails, [journal d’audit](https://experienceleague.adobe.com/docs/marketo/using/product-docs/administration/audit-trail/audit-trail-overview.html), et [journal des activités](https://experienceleague.adobe.com/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/managing-people-in-smart-lists/locate-the-activity-log-for-a-person.html) pour obtenir le contexte.
4. Gagnez du temps lors du transfert [!DNL Marketo Engage] connaissance d’une nouvelle [!DNL Marketo Engage] administrateur si votre équipe connaît un chiffre d’affaires.

## [!DNL Marketo Engage] guide de gouvernance 101

Un guide de gouvernance sert de source de vérité pour la configuration de l’instance et les exigences de conception du système. Les informations clés recommandées à inclure dans ce document sont les suivantes :

* Structures de programme/dossier
* Autorisation utilisateur et rôle
* Limites de communication
* Normes de gouvernance
* Formation des utilisateurs internes avant de leur accorder l’accès à la plateforme

## Comment développer et gérer un guide de gouvernance pour votre [!DNL Marketo Engage] instance

### Étape 1 : Identifiez votre guide et votre documentation actuels sur l’état de gouvernance

* **Je ne parviens pas à trouver de documentation pour mon instance héritée :** Si vous avez récemment démarré un nouveau rôle et que vous ne parvenez pas à trouver la documentation de votre instance héritée, **passer à l’étape 2** et commencez avec un modèle téléchargeable que nous avons fourni.
* **Je dispose de la documentation sur le fichier :** Félicitations, c&#39;est un bon signe ! Veillez à vérifier leur pertinence pour savoir quand la dernière modification est effectuée. S’il n’est pas activement géré par les membres de votre équipe, il est recommandé de les actualiser et d’informer vos utilisateurs internes sur la manière de le tenir à jour.

### Étape 2 : Identifiez les éléments à inclure dans votre [!DNL Marketo Engage] Documentation et [!DNL Changelogs]

Le format varie d’une plateforme basée sur le cloud à un document partagé. Vous pouvez concevoir le format qui répond aux besoins de votre entreprise. [Voici une documentation simple et un modèle Excel de modification](/help/tutorial-inherited-instance/_assets/downloads/Adobe_Marketo_Engage_Inherited_Instance_Documentation-Changlog.xlsx) couvrant les éléments importants que vous pouvez utiliser. Voici quelques-unes de ces fonctions :

* Documentation
   * Nom du modèle de programme
   * Canal
   * Date de création
   * Créé par
   * Objectif du programme
   * Statut
   * Lien vers le modèle de programme
   * Noter
* Changelog
   * Nom du modèle de programme
   * Date de changement
   * Mis à jour par
   * Objectif de la mise à jour
   * Expérience avant modification (inclure des liens/captures d’écran)
   * Expérience après modification (inclure des liens/captures d’écran)
   * URL du programme

### Étape 3 : identifier et documenter l&#39;état actuel des programmes opérationnels principaux

Commencez par identifier les programmes opérationnels clés ayant un impact au niveau de l’abonnement. Par exemple, les campagnes de Data Management, le cycle de vie des pistes, la notation des pistes, [!DNL CRM] Synchronisation et délivrabilité.

Pour chaque programme opérationnel identifié, documentez son état actuel. Cela inclut des détails sur l’objectif du programme, la configuration, les campagnes intelligentes associées et l’intégration à d’autres outils (le cas échéant).

### Étape 4 : Application [!DNL Changelog] Maintenance

L’étape suivante consiste à établir une politique de gouvernance stricte pour votre [!DNL Marketo Engage] instance qui requiert &quot;[!DNL Changelog] maintenance.&quot; Cette politique garantit que toutes les mises à jour apportées aux programmes opérationnels dans l’instance sont entièrement documentées.

Eduquez votre équipe sur l&#39;importance de ces documents et comment y accéder et les mettre à jour correctement. Il peut s’avérer utile d’attribuer des responsabilités pour la gestion du journal des modifications. Ainsi, quelques membres ou administrateurs désignés de l’équipe des opérations marketing enregistrent régulièrement les modifications et fournissent des signatures.

### Étape 5 : Centralisation de la documentation

Créez un emplacement central ou un référentiel pour stocker toute la documentation relative à votre [!DNL Marketo Engage] instance. Il peut s’agir d’un lecteur partagé, d’un dossier dédié ou d’un système basé sur le cloud.

### Étape 6 : Révision et mise à jour régulières

Planifiez des révisions régulières de votre documentation afin de vous assurer qu’elle reste exacte et à jour. On peut facilement l&#39;ignorer pendant les heures de pointe. Configurez de manière proactive des rappels sur votre calendrier afin de vous assurer que votre équipe effectue régulièrement des mises à jour pour refléter les modifications ou les optimisations de vos programmes opérationnels.

## Et après ?

Commencer en téléchargeant ceci [modèle simple](/help/tutorial-inherited-instance/_assets/downloads/Adobe_Marketo_Engage_Inherited_Instance_Documentation-Changlog.xlsx).

Suivez les étapes ci-dessus pour développer votre guide de gouvernance et votre documentation. Pendant que vous effectuez le processus, tenez compte des règles de base suivantes :

**Mettez à jour votre documentation existante :**
Il est essentiel de garder votre documentation à jour. S’il n’a pas été modifié depuis 3 ans, prenez le temps de réviser votre documentation au fur et à mesure que vous contrôlez votre instance.

**Partager et entraîner :**
Partager votre documentation et [!DNL changelog] avec les membres de l’équipe concernés et apprenez-les à mettre à jour ces enregistrements.

**Examen périodique :** prévoir le temps nécessaire pour les passer en revue et les gérer tout au long de l’année afin d’inclure tout nouveau changement, optimisation ou ajustement au fur et à mesure.

La maintenance d’une documentation complète et à jour pour votre instance de Marketo Engage vous fera gagner du temps et vous fera gagner du temps et vous aidera à gérer efficacement les instances.

### Auteurs

**Nick Hajdin**
[!DNL Adobe Marketo Champion] (2018)
*[!DNL Digital Technology Senior Manager at Accenture]*

![Nick Hajdin](/help/tutorial-inherited-instance/_assets/authors/Customer_Author_Nicholas_Hajdin.png){width="30%"}

**Amy Chiu**
*Gestionnaire marketing de l’adoption et de la rétention, Adobe*

![Amy Chiu](/help/tutorial-inherited-instance/_assets/authors/Adobe_Author_Amy_Chiu.png){width=30%}
