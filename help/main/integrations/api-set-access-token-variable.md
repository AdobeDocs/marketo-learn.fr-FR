---
title: Vidéo sur l’API Marketo - Comment définir le jeton d’accès dans une variable
description: Découvrez comment configurer l’application Postman et comment exploiter les variables pour enregistrer les données dans la variable à des fins de réutilisation.
feature: REST API
role: Admin, Developer
level: Experienced
doc-type: Technical Video
duration: 772
last-substantial-update: 2024-08-06T00:00:00Z
jira: KT-15548
exl-id: 4da86ed6-1072-4e0e-a648-16587badaeb3
source-git-commit: 9bffa576fc5a05c695f7a1c83d50cbcb16f57c37
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 27%

---

# Assistance API : comment définir le jeton d’accès dans une variable

Découvrez comment configurer l’application Postman et utiliser les variables pour enregistrer les données dans la variable à des fins de réutilisation. Découvrez également comment effectuer votre premier appel API REST Marketo Engage pour obtenir le jeton d’accès.

>[!PREREQUISITES]
>
>Avant de commencer cette vidéo, créez un nom d’utilisateur API uniquement avec un rôle API et créez un service Launchpad. Suivez les étapes décrites dans les articles ci-dessous :
>
>* [Créer un rôle d’utilisateur API uniquement](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/users-and-roles/create-an-api-only-user-role){target="_blank"}
>
>* [Créer un utilisateur API uniquement](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/users-and-roles/create-an-api-only-user){target="_blank"}
>
>* [Créer un service personnalisé à utiliser avec l’API REST](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/additional-integrations/create-a-custom-service-for-use-with-rest-api){target="_blank"}

**Références utilisées dans cette vidéo :**

* Point d’entrée d’authentification Marketo : `{{{}base_url{}}}/identity/oauth/token?grant_type=client_credentials&client_id={{{}client_id{}}}&client_secret={{{}client_secret{}}}`

* Script JS pour récupérer access_token à partir du corps de la réponse (emplacement sous l’onglet Scripts : ) :

```
var jsonData = pm.response.json();
pm.environment.set("access_token", jsonData.access_token);
```

* [Documentation destinée aux développeurs de Marketo Engage](https://experienceleague.adobe.com/fr/docs/marketo-developer/marketo/rest/authentication){target="_blank"}

>[!VIDEO](https://video.tv.adobe.com/v/3429275/?learn=on)
