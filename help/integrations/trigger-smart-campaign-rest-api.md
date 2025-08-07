---
title: Tutoriel - Déclenchement d’une campagne intelligente dans Marketo Engage à l’aide de l’API REST et de jetons
description: Découvrez comment déclencher une campagne intelligente dans Marketo Engage à l’aide de l’API REST et personnaliser l’e-mail à l’aide de Mes jetons.
feature: REST API
role: Admin, Developer
level: Experienced
exl-id: 46e54729-92ab-4bbb-9877-f762708def67
source-git-commit: 99058de9712fbebd631215ef15a6df349ca4c3cc
workflow-type: tm+mt
source-wordcount: '611'
ht-degree: 1%

---

# Déclenchement d’une campagne intelligente dans Marketo Engage à l’aide de l’API REST et de jetons

Ce tutoriel vous explique comment déclencher une campagne intelligente dans Marketo Engage à l’aide de l’API REST et personnaliser l’e-mail à l’aide de Mes jetons. Ce cas d’utilisation est idéal pour les notifications déclenchées par le client comme les rappels de webinaire, les étapes d’intégration ou les suivis après achat.

## Cas d’utilisation {#use-case}

Une personne s’inscrit à un webinaire par le biais d’une plateforme externe (par exemple, une application personnalisée, Pendo, Eventbrite). Vous souhaitez effectuer automatiquement les opérations suivantes :

* Déclencher un e-mail de rappel depuis Marketo Engage
* Personnalisez-le avec :
   * Prénom de la personne
   * Titre du webinaire
   * Un lien de jointure unique

Vous pouvez le faire à l’aide de l’API REST et de Mes jetons.

## Étape 1 : créer la campagne intelligente {#step-one}

1. Accédez à **Activités marketing**, puis dans votre dossier [Programmes](https://experienceleague.adobe.com/fr/docs/marketo/using/product-docs/core-marketo-concepts/programs/creating-programs/understanding-programs){target="_blank"}, créez une [Campagne intelligente](https://experienceleague.adobe.com/fr/docs/marketo/using/product-docs/core-marketo-concepts/smart-campaigns/understanding-smart-campaigns){target="_blank"} appelée `Send Webinar Reminder`.

1. Dans l&#39;onglet **Smart List** , [ajoutez un déclencheur](https://experienceleague.adobe.com/fr/docs/marketo/using/product-docs/core-marketo-concepts/smart-campaigns/creating-a-smart-campaign/define-smart-list-for-smart-campaign-trigger){target="_blank"} pour permettre l&#39;appel de la campagne via l&#39;API :

   * Sélectionnez **Campagne demandée** comme déclencheur
   * Définir le **Source** sur `Web Service API`

![Configuration du déclencheur de liste dynamique](assets/trigger-smart-campaign-rest-api-1.png)

## Étape 2 : définir le contenu de l’e-mail {#step-two}

Créez ou modifiez une [ressource e-mail](https://experienceleague.adobe.com/fr/docs/marketo-developer/marketo/rest/assets/emails){target="_blank"} qui fait référence à la fois à la personne et à [Mes jetons](https://experienceleague.adobe.com/fr/docs/marketo/using/product-docs/core-marketo-concepts/programs/tokens/managing-my-tokens){target="_blank"}.

>[!NOTE]
>
>Veillez à insérer les jetons directement dans le contenu de l’e-mail, comme illustré ci-dessous.

```html
Hi {{lead.First Name:default=Customer}}

You're registered for **{{my.WebinarTitle}}**.

Join here: {{my.JoinLink}}
```

Si vous utilisez un jeton pour injecter dynamiquement une URL d’image (par exemple, `{{my.WebinarImage}}`), vous devez encapsuler le jeton dans une balise d’image HTML :

```html
<img src="{{my.WebinarImage}}" alt="Webinar banner" />
```

>[!IMPORTANT]
>
>Marketo Enagage **ne rendra pas**’image à moins que le jeton ne soit placé dans une balise d’image valide.

![Éditeur d’e-mail affichant l’utilisation des jetons](assets/trigger-smart-campaign-rest-api-2.png)

## Étape 3 : ajouter des jetons au programme {#step-three}

Pour transmettre des valeurs de manière dynamique via l’API, les jetons doivent déjà exister dans Marketo Engage. Vous devrez les créer sous l’onglet **Mes jetons** de votre programme.

1. Accédez à l’onglet **Mes jetons** de votre programme parent.

2. Faites glisser un **jeton de texte** depuis le panneau de droite pour chaque valeur dynamique.

* `{{my.WebinarTitle}}` - Jeton de texte
* `{{my.JoinLink}}` - Jeton de texte
* `{{my.WebinarImage}}` - Jeton de texte (il sera utilisé comme `src` dans une balise `<img>`)

![Onglet Mes jetons dans la campagne](assets/trigger-smart-campaign-rest-api-3.png)

## Étape 4 : définir les règles de qualification de la campagne et activer la campagne {#step-four}

1. Configurez les [règles de qualification](https://experienceleague.adobe.com/fr/docs/marketo/using/product-docs/core-marketo-concepts/smart-campaigns/using-smart-campaigns/edit-qualification-rules-in-a-smart-campaign){target="_blank"} pour contrôler la fréquence à laquelle une personne peut exécuter la campagne intelligente.

1. Une fois la configuration terminée, cliquez sur **Activer** pour permettre à la campagne intelligente de recevoir les requêtes déclenchées par l’API.

![Règle de qualification de campagne intelligente](assets/trigger-smart-campaign-rest-api-4.png)

## Étape 5 : déclencher la campagne via l’API REST {#step-five}

### Trouver l’identifiant de la campagne {#find-the-campaign-id}

Pour déclencher une campagne dynamique à l’aide de l’API, vous devez disposer de l’identifiant **campaign** :

1. Recherchez et sélectionnez la campagne intelligente à déclencher.

1. Examinez l’URL dans votre navigateur. Il ressemblera à ceci : `https://app-XXX.marketo.com/#/classic/SC`**1234**`A1ZN38`.

1. Les 4 chiffres après `SC` représentent votre identifiant de campagne. Dans l’exemple ci-dessus, l’identifiant de campagne intelligente est « 1234 »

Utilisez le point d’entrée suivant :

```
POST /rest/v1/campaigns/{campaignId}/trigger.json
```

Exemple :

```
POST /rest/v1/campaigns/1234/trigger.json
```

### Exemple de corps de requête {#example-request-body}

```json
{
  "input": {
    "leads": [
      {
        "id": 1002200
      }
    ],
    "tokens": [
      {
        "name": "{{my.WebinarTitle}}",
        "value": "Scaling Customer Engagement in 2025"
      },
      {
        "name": "{{my.JoinLink}}",
        "value": "https://webinars.company.com/join/abc123"
      },
      {
        "name": "{{my.WebinarImage}}",
        "value": "https://experienceleague.adobe.com/fr/docs/marketo-learn/tutorials/events/media_1c6f338a518ada11550084c8ab3a6bbf554ff6eac.jpeg"
      }
    ]
  }
}
```

>[!IMPORTANT]
>
>Remplacez `1002200` dans l’exemple de corps ci-dessus par l’ID de personne correct de votre instance Marketo Engage.

## Autorisation {#authorization}

Toutes les requêtes d’API REST Marketo nécessitent un jeton d’accès OAuth 2.0.

Pour récupérer votre jeton d’accès, utilisez le point d’entrée suivant :

```
GET /identity/oauth/token?grant_type=client_credentials&client_id=XXX&client_secret=YYY
```

Une fois que vous avez reçu votre jeton d’accès, incluez-le en tant que _paramètre de requête_ dans toutes les requêtes API :

```
Authorization: Bearer YOUR_ACCESS_TOKEN
```

## Meilleures pratiques {#best-practices}

* Ajoutez des valeurs de secours/par défaut à vos jetons pour le test et l’assurance qualité.
* Utiliser des `{{lead.token}}` pour les champs de personne et des `{{my.token}}` pour les valeurs dynamiques de la campagne
* Marketo Engage prend en charge jusqu’à 100 personnes par demande
* Les personnes doivent répondre aux critères de la liste dynamique, sinon elles sont silencieusement ignorées.

## Résumé {#summary}

Grâce à cette approche, vous pouvez personnaliser les communications à l’aide de campagnes intelligentes déclenchées à partir de plateformes externes via l’API. Cela s’avère utile pour des scénarios tels que les confirmations d’enregistrement à un webinaire, les e-mails d’intégration et les notifications transactionnelles, tout en injectant des données en temps réel à l’aide de Mes jetons.
