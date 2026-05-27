---
title: Développement d’un guide de gouvernance des instances avec documentation
description: Découvrez comment établir une procédure robuste pour créer et gérer la documentation et le journal des modifications pour votre instance Marketo Engage. Cela permet non seulement de gagner du temps pour le partage des connaissances de votre équipe, mais également d’améliorer l’intégrité et l’efficacité de votre instance.
feature: Administration
role: Admin
level: Intermediate, Experienced
doc-type: Tutorial
last-substantial-update: 2023-10-16T00:00:00.000Z
jira: KT-14103
thumbnail: KT-14103.jpeg
index: true
exl-id: 4313b54a-1848-4684-b037-7a7795dd01ec
TQID: https://experienceleague.adobe.com/t1TtyyanSwdY8cE3hEkLLOqIW2GpEvFUS1I4LGpUnKM
product_v2: id: b27e5950-9033-45ac-9f86-eb22e567f615
feature_v2: id: a7170d27-32ab-462b-a333-269abc654483id: d1d0a9cd-295d-4976-8c39-ddae266f240eid: e64968b2-4ee5-47f9-8cae-0588f184b9eb
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0f8ea3988fd586ccbd4b414b3558f6e5f36882bf
workflow-type: tm+mt
source-wordcount: 959
ht-degree: 1%

---

# Développement d’un guide de gouvernance des instances avec documentation

Lorsque vous passez à une instance de [!DNL Marketo Engage] héritée, le défi consiste souvent à manquer d’une documentation fonctionnelle et technique à jour. En tant qu’administrateur, vous ne pouvez pas négliger la nécessité d’établir des directives pour garantir une gouvernance d’instance appropriée. Il s’agit de l’une des stratégies essentielles pour [accroître l’efficacité lorsque vous travaillez dans une instance Marketo Engage établie](https://nation.marketo.com/t5/champion-program-blogs/3-tips-to-increase-your-efficiency-in-an-inherited-instance/ba-p/247582).

Ce tutoriel détaillé provenant de [!DNL Adobe Marketo Champion] (2018), Nick Hajdin, vous guidera tout au long de ce processus pour décrire la configuration de votre instance, documenter vos principaux programmes opérationnels et maintenir une [!DNL changelog] pour appliquer une politique de gouvernance stricte.

## Pourquoi développer un guide de gouvernance d’instance et de la documentation pour votre instance héritée ?

Une documentation détaillée et un [!DNL changelog] sont essentiels pour une gestion efficace et un transfert des connaissances au sein de votre instance [!DNL Marketo Engage]. Suivre les modifications et les décisions que vous avez prises lors de la configuration de votre instance peut vous aider à :

1. Formez plus facilement les utilisateurs internes de manière évolutive.
2. Construire plus efficacement en [!DNL Marketo Engage] à long terme.
3. Maintenez l’intégrité et l’hygiène de votre instance à l’avenir afin d’éviter de passer des heures à creuser dans les e-mails, [journal d’audit](https://experienceleague.adobe.com/docs/marketo/using/product-docs/administration/audit-trail/audit-trail-overview.html) et [journal d’activité](https://experienceleague.adobe.com/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/managing-people-in-smart-lists/locate-the-activity-log-for-a-person.html) pour obtenir du contexte.
4. Gagnez du temps lors du transfert de [!DNL Marketo Engage] connaissances à un nouvel administrateur [!DNL Marketo Engage] si votre équipe fait l’objet d’un roulement.

## Guide de gouvernance [!DNL Marketo Engage] 101

Un guide de gouvernance sert de source de vérité pour la configuration des instances et les exigences de conception du système. Il est recommandé d’inclure les informations clés suivantes dans ce document :

* Structures de programmes/dossiers
* Autorisation Utilisateur et rôle
* Limites de communication
* Normes de gouvernance
* Formation interne des utilisateurs avant de leur accorder l&#39;accès à la plateforme

## Développement et gestion d’un guide de gouvernance pour votre instance [!DNL Marketo Engage]

### Étape 1 : identifier votre guide et votre documentation actuels sur l’état de la gouvernance

* **Je ne trouve aucune documentation pour mon instance héritée :** si vous avez récemment démarré un nouveau rôle et ne parvenez pas à trouver de documentation pour votre instance héritée, **passez à l’étape 2** et commencez à utiliser un modèle téléchargeable que nous avons fourni.
* **J’ai de la documentation dans mes dossiers :** Félicitations, c’est bon signe ! Veillez à vérifier leur pertinence pour voir quand la dernière modification est apportée. S’il n’est pas géré activement par les membres de votre équipe, il est recommandé de l’actualiser et d’éduquer vos utilisateurs internes sur la manière de le tenir à jour.

### Étape 2 : identifier les éléments à inclure dans votre documentation et [!DNL Changelogs] [!DNL Marketo Engage]

Le format varie d’une plateforme cloud à un document partagé. Vous pouvez concevoir le format qui répond aux besoins de votre entreprise. [Voici un modèle Excel de documentation et de journal des modifications simple](/help/tutorial-inherited-instance/_assets/downloads/Adobe_Marketo_Engage_Inherited_Instance_Documentation-Changlog.xlsx) couvrant les éléments importants avec lesquels vous pouvez commencer. Ces cas comprennent notamment :

* Documentation
   * Nom du modèle de programme
   * Canal
   * Date de création
   * Créée par
   * Objectif du programme
   * Statut
   * Lien vers le modèle de programme
   * Remarque
* Journal des modifications
   * Nom du modèle de programme
   * Date of Change
   * Mise à jour par
   * Objectif de la mise à jour
   * Expérience avant modification (inclure des liens/captures d’écran)
   * Expérience après modification (inclure des liens/captures d’écran)
   * URL vers le programme

### Étape 3 : Recenser et documenter l&#39;état actuel des programmes opérationnels primaires

Commencez par identifier les programmes opérationnels clés ayant un impact au niveau des abonnements. Par exemple, les campagnes de gestion des données, le cycle de vie des leads, la notation des leads, la synchronisation des [!DNL CRM] et la délivrabilité.

Pour chaque programme opérationnel identifié, documenter son état actuel. Cela inclut des détails sur l’objectif du programme, sa configuration, les campagnes intelligentes associées et l’intégration à d’autres outils (le cas échéant).

### Étape 4 : appliquer la maintenance [!DNL Changelog]

L’étape suivante consiste à établir une politique de gouvernance stricte pour votre instance [!DNL Marketo Engage] qui rend obligatoire la « maintenance [!DNL Changelog] ». Cette politique garantit que toutes les mises à jour apportées aux programmes opérationnels dans l’instance sont entièrement documentées.

Sensibilisez votre équipe à l’importance de ces documents et à la manière d’y accéder et de les mettre à jour correctement. Il peut s&#39;avérer utile d&#39;affecter des responsabilités à la gestion du journal des modifications, de sorte que quelques membres de l&#39;équipe ou administrateurs de l&#39;opération marketing enregistrent régulièrement les modifications et fournissent des approbations.

### Étape 5 : Centralisation De La Documentation

Définissez un emplacement ou un référentiel central pour stocker toute la documentation relative à votre instance [!DNL Marketo Engage]. Il peut s’agir d’un lecteur partagé, d’un dossier dédié ou d’un système basé sur le cloud.

### Étape 6 : Examen et mise à jour réguliers

Planifiez des révisions régulières de votre documentation pour vous assurer qu’elle reste précise et à jour. Il peut être facilement négligé pendant les heures d&#39;affluence. Mettez en place des rappels de manière proactive sur votre calendrier pour vous assurer que votre équipe effectue régulièrement des mises à jour afin de refléter les modifications ou optimisations apportées à vos programmes opérationnels.

## Quelle est la suite ?

Commencez par télécharger ce [modèle simple](/help/tutorial-inherited-instance/_assets/downloads/Adobe_Marketo_Engage_Inherited_Instance_Documentation-Changlog.xlsx).

Suivez les étapes ci-dessus pour développer votre guide de gouvernance et votre documentation. Tout au long du processus, gardez à l’esprit les règles suivantes :

**Mettez à jour votre documentation existante :**
Il est essentiel de garder votre documentation à jour. S’il n’a pas été modifié au cours des 3 dernières années, consacrez du temps à la révision de votre documentation au fur et à mesure que vous auditez votre instance.

**Partager et former :**
Partagez votre documentation et vos [!DNL changelog] avec les membres de l’équipe concernés et apprenez-leur comment mettre à jour ces enregistrements.

**Révision périodique :** planifiez une période de révision et de maintenance tout au long de l’année afin d’inclure les nouvelles modifications, optimisations ou ajustements au fur et à mesure qu’ils se produisent.

Maintenir une documentation complète et à jour pour votre instance Marketo Engage vous permet de gagner du temps et vous évite des efforts à long terme et facilite une gestion efficace des instances.

### Auteurs

**Nick Hajdin**
[!DNL Adobe Marketo Champion] (2018)
*[!DNL Digital Technology Senior Manager at Accenture]*

![ Nick Hajdin ](/help/tutorial-inherited-instance/_assets/authors/Customer_Author_Nicholas_Hajdin.png){width="30%"}

**Amy Chiu**
*Responsable marketing adoption et rétention, Adobe*

![ Amy Chiu ](/help/tutorial-inherited-instance/_assets/authors/Adobe_Author_Amy_Chiu.png){width=30%}
