---
title: Vidéo sur l’API Marketo - Comment définir le jeton d’accès dans une variable
description: Découvrez comment configurer l’application Postman et comment exploiter les variables pour enregistrer les données dans la variable à des fins de réutilisation.
feature: REST API
role: Admin, Developer
level: Experienced
doc-type: Technical Video
duration: 772
last-substantial-update: 2024-08-06T00:00:00.000Z
jira: KT-15548
exl-id: 4da86ed6-1072-4e0e-a648-16587badaeb3
product_v2:
  - id: b27e5950-9033-45ac-9f86-eb22e567f615
    internal-label: Marketo Engage
feature_v2:
  - id: dca84292-69e9-4116-a575-667d31fa060d
    internal-label: APIs
subfeature_v2:
  - id: cf1396d8-ab85-4e93-b35d-d9b573024abf
    internal-label: REST APIs
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
source-git-commit: 4768ecb20d4d9c70452ae084256928261f3a80eb
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
