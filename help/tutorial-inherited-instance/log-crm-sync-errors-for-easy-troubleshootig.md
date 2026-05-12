---
title: Consigner les erreurs de synchronisation CRM pour faciliter le dépannage
description: Découvrez comment utiliser un journal des erreurs de synchronisation CRM pour examiner les problèmes de synchronisation CRM et assurer son bon fonctionnement.
feature: Administration
role: Admin
level: Intermediate, Experienced
doc-type: Tutorial
last-substantial-update: 2023-10-16T00:00:00.000Z
jira: KT-13875
thumbnail: KT-13875.jpeg
index: true
exl-id: 3b7e6127-28fd-4dce-915d-5af9bcce984b
TQID: https://experienceleague.adobe.com/JM26ZReC9P8rKS8IqjIV5TKLxT0xInUHysdM7zo0LzM
product_v2: id: b27e5950-9033-45ac-9f86-eb22e567f615
feature_v2: id: d1d0a9cd-295d-4976-8c39-ddae266f240e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0f8ea3988fd586ccbd4b414b3558f6e5f36882bf
workflow-type: tm+mt
source-wordcount: 470
ht-degree: 0%

---

# Consigner les erreurs de synchronisation CRM pour faciliter le dépannage

En tant qu’administrateur Marketo Engage, la vérification de la synchronisation de votre instance avec votre CRM doit être un élément essentiel de votre [routine quotidienne](https://nation.marketo.com/t5/champion-program-blogs/my-marketo-morning-routine-tips-for-driving-marketing-operation/ba-p/247508){target="_blank"}. Bien que la [section Notifications](https://experienceleague.adobe.com/docs/marketo/using/product-docs/core-marketo-concepts/miscellaneous/notification-types.html){target="_blank"} (située dans le coin supérieur droit de votre interface Marketo Engage) soit l’endroit où vous commencerez à rechercher et à étudier les problèmes de synchronisation fréquents, il existe une astuce pour vous aider à gérer l’intégrité de l’instance de manière organisée. Championne Adobe Marketo (2019-2022), Amy Goldfine recommande aux administrateurs de tenir un journal des erreurs de synchronisation CRM pour faciliter la résolution des problèmes.

![Capture d’écran de l’onglet Erreurs de synchronisation](/help/tutorial-inherited-instance/_assets/Marketo_Engage_Admin_Salesforce_Sync_Errors_Tab.png)

## Pourquoi conserver un enregistrement des erreurs de synchronisation CRM ?

En consignant les erreurs de synchronisation CRM, les administrateurs Marketo Engage peuvent examiner les problèmes et les tendances avec les administrateurs CRM pour résoudre la cause première. Suivez les étapes ci-dessous pour documenter vos problèmes de synchronisation CRM pour votre instance.

## Comment conserver un journal des erreurs de synchronisation CRM

Avant de commencer, téléchargez le modèle de journal [Erreurs de synchronisation CRM](/help/tutorial-inherited-instance/_assets/downloads/Adobe-Marketo-Engage_CRM-Sync-Error-Log-Template.xlsx).

**Étape 1 :** à la section *[!UICONTROL Admin] dans Marketo Engage*. Sous *[!UICONTROL Intégration]*, cliquez sur *[!DNL Salesforce]*, *[!DNL Microsoft Dynamics]* ou *[!DNL Veeva]*, selon le [!DNL CRM] utilisé, puis sur l’onglet *[!UICONTROL Erreurs de synchronisation]*.

**Étape 2 :** vous pouvez choisir d’[exporter les enregistrements d’erreurs sous forme  [!DNL CSV]  fichier via le panneau [!UICONTROL Filtrer]](https://experienceleague.adobe.com/docs/marketo/using/product-docs/crm-sync/salesforce-sync/salesforce-sync-errors.html#filter-sync-errors){target="_blank"}. Si vous ne disposez que de quelques heures, il est recommandé de copier et coller directement à partir de l’onglet *[!UICONTROL Erreurs de synchronisation]*.

**Étape 3 :** Notez la date à laquelle l’erreur s’est produite.

**Étape 4 :** saisissez le nombre d’enregistrements de personne affectés par cette erreur. (Parfois, votre CRM ne renvoie une erreur que pour une seule personne. Parfois, il y aura plusieurs personnes avec la même erreur à la fois.)

**Étape 5 :** notez l’adresse e-mail d’une personne affectée par l’erreur. Vous pouvez ainsi facilement référencer les erreurs et en discuter avec l’administrateur CRM.

**Étape 6 :** coller des liens vers l’enregistrement de personne dans [!DNL Marketo Engage] et [!UICONTROL Lead/Contact CRM] l’enregistrement de cette personne.

**Étape 7 :** dans la dernière colonne, collez le texte réel de l’erreur.

## Quelle est la suite ?

**Identifier les codes d’erreur :** pour comprendre les codes d’erreur, consultez les descriptions de la documentation destinée aux développeurs [tableau Codes d’erreur au niveau de la réponse](https://developers.marketo.com/rest-api/error-codes/#response_level_error_codes){target="_blank"} et recherchez les étapes suivantes standard pour résoudre les erreurs.

## Auteurs

**Amy Goldfine**\
Adobe Marketo Champion(2019-2022)
*fondateur, MarketingOpsAdvice.com*

![ Amy Goldfine ](/help/tutorial-inherited-instance/_assets/authors/Customer_Author_Amy_Goldfine.png){width="25%"}

**Amy Chiu**
*Responsable marketing adoption et rétention chez Adobe*

![ Amy Chiu ](/help/tutorial-inherited-instance/_assets/authors/Adobe_Author_Amy_Chiu.png){width="25%"}
