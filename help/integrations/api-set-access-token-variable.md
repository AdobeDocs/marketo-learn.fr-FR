---
title: Vidéo de présentation de l’API Marketo - Comment définir le jeton d’accès dans une variable
description: Découvrez comment configurer l’application Postman et comment utiliser des variables pour enregistrer des données dans la variable à des fins de réutilisation.
feature: REST API
role: Admin, Developer
level: Beginner
doc-type: Technical Video
duration: 772
last-substantial-update: 2024-08-06T00:00:00Z
jira: KT-15548
source-git-commit: 757f21c965161fba774c2c31e02baa75f4691e4d
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---


# Aide de l’API - Comment définir le jeton d’accès dans une variable

Découvrez comment configurer l’application Postman et utiliser les variables pour enregistrer les données dans la variable à des fins de réutilisation. Vous apprendrez également comment effectuer votre premier appel API REST Marketo Engage pour obtenir le jeton d’accès.

>[!PREREQUISITES]
>
>Avant de commencer cette vidéo, créez un nom d’utilisateur API uniquement avec un rôle AOI et créez un service Launchpad. Suivez les étapes décrites dans les articles ci-dessous :
>
>* [Création d’un rôle d’utilisateur API unique](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/users-and-roles/create-an-api-only-user-role){target="_blank"}
>
>* [Créer un utilisateur API uniquement](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/users-and-roles/create-an-api-only-user){target="_blank"}
>
>* [ Créez un service personnalisé à utiliser avec l’API REST ](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/additional-integrations/create-a-custom-service-for-use-with-rest-api){target="_blank"}

**Références utilisées dans cette vidéo :**

* Point d’entrée de l’authentification Marketo : `{{{}base_url{}}}/identity/oauth/token?grant_type=client_credentials&client_id={{{}client_id{}}}&client_secret={{{}client_secret{}}}`

* Script JS pour récupérer access_token du corps de la réponse (places sous l’onglet Scripts: ) :

`var jsonData = pm.response.json();
pm.environment.set("access_token", jsonData.access_token);`

* [Documentation pour les développeurs Marketo Engage](https://experienceleague.adobe.com/en/docs/marketo-developer/marketo/rest/authentication){target="_blank"}

>[!VIDEO](https://video.tv.adobe.com/v/3429275/?learn=on)
