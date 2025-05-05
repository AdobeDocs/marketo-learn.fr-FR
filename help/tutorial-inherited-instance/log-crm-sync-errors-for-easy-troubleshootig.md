---
title: Enregistrer les erreurs de synchronisation CRM pour faciliter le dépannage
description: Découvrez comment utiliser un journal des erreurs de synchronisation CRM pour étudier les problèmes de synchronisation CRM et le maintenir en bon état.
feature: Administration
role: Admin
level: Intermediate, Experienced
doc-type: Tutorial
last-substantial-update: 2023-10-16T00:00:00Z
jira: KT-13875
thumbnail: KT-13875.jpeg
hide: false
exl-id: 3b7e6127-28fd-4dce-915d-5af9bcce984b
source-git-commit: 681d390ce5ab336a7e24cc63256659a492288517
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 0%

---

# Enregistrer les erreurs de synchronisation CRM pour faciliter le dépannage

En tant qu&#39;administrateur de Marketo Engage, vérifier si votre instance est synchronisée avec votre CRM doit être un élément clé de votre [routine quotidienne](https://nation.marketo.com/t5/champion-program-blogs/my-marketo-morning-routine-tips-for-driving-marketing-operation/ba-p/247508){target="_blank"}. Bien que la [section Notifications](https://experienceleague.adobe.com/docs/marketo/using/product-docs/core-marketo-concepts/miscellaneous/notification-types.html?lang=fr){target="_blank"} (la trouve dans le coin supérieur droit de l’interface de votre Marketo Engage) soit l’endroit où vous allez commencer à rechercher et à étudier les problèmes de synchronisation fréquents, il existe une astuce pro qui peut vous aider à gérer l’intégrité de l’instance de manière organisée. Champion Marketo Adobe (2019-2022), Amy Goldfine recommande aux utilisateurs administrateurs de conserver un journal des erreurs de synchronisation CRM afin de faciliter le dépannage.

![Capture d’écran de l’onglet Erreurs de synchronisation](/help/tutorial-inherited-instance/_assets/Marketo_Engage_Admin_Salesforce_Sync_Errors_Tab.png)

## Pourquoi conserver un enregistrement des erreurs de synchronisation CRM ?

En consignant les erreurs de synchronisation CRM, les administrateurs de Marketo Engage peuvent consulter les problèmes et tendances avec les administrateurs CRM pour résoudre la cause principale. Suivez les étapes ci-dessous pour documenter les problèmes de synchronisation CRM pour votre instance.

## Comment conserver un journal des erreurs de synchronisation CRM

Avant de commencer, téléchargez le [modèle Journal des erreurs de synchronisation CRM](/help/tutorial-inherited-instance/_assets/downloads/Adobe-Marketo-Engage_CRM-Sync-Error-Log-Template.xlsx).

**Étape 1 :** Accédez à la section *[!UICONTROL Admin]* en Marketo Engage. Sous *[!UICONTROL Intégration]*, cliquez sur *[!DNL Salesforce]*, *[!DNL Microsoft Dynamics]* ou *[!DNL Veeva]*, en fonction de l’élément [!DNL CRM] que vous utilisez, puis sur l’onglet *[!UICONTROL Erreurs de synchronisation]*.

**Étape 2 :** Vous pouvez choisir [ d&#39;exporter les enregistrements des erreurs sous la forme d&#39;un fichier  [!DNL CSV] par le biais du [!UICONTROL panneau de filtre]](https://experienceleague.adobe.com/docs/marketo/using/product-docs/crm-sync/salesforce-sync/salesforce-sync-errors.html?lang=fr#filter-sync-errors){target="_blank"}. Si vous ne disposez que de quelques heures, vous pouvez choisir de copier et coller directement à partir de l’onglet *[!UICONTROL Erreurs de synchronisation]*.

**Étape 3 :** Notez la date à laquelle l’erreur s’est produite.

**Étape 4 :** Saisissez le nombre d’enregistrements de personne concernés par cette erreur. (Parfois, votre CRM ne génère une erreur que pour une seule personne. Parfois, il y aura beaucoup de gens avec la même erreur à la fois.)

**Étape 5 :** Notez l’adresse électronique d’une personne affectée par l’erreur. Cela facilite la référence et la discussion des erreurs avec l&#39;administrateur CRM.

**Étape 6 :** Le collage des liens vers l’enregistrement de la personne dans [!DNL Marketo Engage] et l’enregistrement [!UICONTROL Lead/contact CRM] de cette personne.

**Étape 7 :** Dans la dernière colonne, collez le texte réel de l’erreur.

## Et après ?

**Identifier les codes d’erreur :** Pour comprendre les codes d’erreur, recherchez les descriptions dans la documentation des développeurs [&#128279;](https://developers.marketo.com/rest-api/error-codes/#response_level_error_codes){target="_blank"} et recherchez les étapes suivantes courantes pour résoudre les erreurs.

## Auteurs

**Amy Goldfine**\
Champion Marketo Adobe (2019-2022)
*Fondateur, MarketingOpsAdvisory.com*

![Amy Goldfine](/help/tutorial-inherited-instance/_assets/authors/Customer_Author_Amy_Goldfine.png){width="25%"}

**Amy Chiu**
*Gestionnaire marketing d’adoption et de rétention à l’Adobe*

![Amy Chiu](/help/tutorial-inherited-instance/_assets/authors/Adobe_Author_Amy_Chiu.png){width="25%"}
