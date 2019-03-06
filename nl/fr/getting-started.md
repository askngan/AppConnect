---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-06"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip} 
{:download: .download}


# Initiation à IBM App Connect
{: #gettingStarted}

{{site.data.keyword.appconservicefull}} vous aide à connecter vos applications, depuis une simple interaction de déclenchement d'action à une intégration complexe. Vous pouvez utiliser {{site.data.keyword.appconserviceshort}} pour créer des flux événementiels ou des flux pour API, ou vous pouvez télécharger et exécuter les solutions d'intégration que vous créez dans IBM Integration Bus, sans avoir à acquérir ou à maintenir une infrastructure informatique. Vous pouvez voir et administrer toutes vos intégrations (serveurs d'intégration, flux événementiels et flux pour API) depuis un seul endroit, sur le tableau de bord d'{{site.data.keyword.appconserviceshort}}. 

Après avoir créé une instance du service {{site.data.keyword.appconserviceshort}}, vous pouvez accéder à {{site.data.keyword.appconserviceshort}} depuis le tableau de bord de {{site.data.keyword.Bluemix}}.

Les étapes suivantes vous fournissent toutes les informations nécessaires pour commencer à utiliser App Connect. Pour obtenir des informations plus détaillées, des guides pratiques sur des applications spécifiques, des tutoriels et des vidéos, consultez la documentation complète sous [IBM App Connect ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://developer.ibm.com/integration/docs/app-connect/).

## Création d'un flux événementiel

Comme son nom l'indique, un flux événementiel est formé par un événement qui déclenche le flux dans une application source et une ou plusieurs actions dans les applications cibles. Lorsqu'un événement se produit dans l'application source, une action est déclenchée dans vos applications cibles. Pour créer un flux événementiel qui connecte vos applications dans le cloud, suivez les étapes suivantes.
1.  Sur le tableau de bord d'{{site.data.keyword.appconserviceshort}}, cliquez sur **New** > **Event-driven flow**.
    {{site.data.keyword.appconserviceshort}} sauvegarde automatiquement les modifications que vous apportez. Si vous sortez du flux à un moment donné, le flux sera sauvegardé à l'état de brouillon et vous pourrez y revenir plus tard.
1.  Entrez un nom pour le flux.
1.  Sélectionnez l'événement déclencheur devant démarrer votre flux en développant une application et en sélectionnant un événement.
1.  Si vous n'êtes pas déjà connecté à votre application, cliquez sur **Connect to _application_** et entrez les détails de connexion de votre application.
    Vous devrez éventuellement fournir des détails de connexion additionnels pour certaines applications. Si vous avez besoin d'aide pour trouver les données d'identification pour une application en particulier, consultez les [guides pratiques des applications ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://developer.ibm.com/integration/docs/app-connect/how-to-guides-for-apps/).
1.  Sélectionnez l'action à déclencher dans votre deuxième application en développant une application et en sélectionnant une action.
    Si nécessaire, cliquez sur **Connect to application** et entrez vos détails de connexion pour l'application cible.
1. Entrez les données que vous souhaitez transférer entre vos applications.
    Vous pouvez ajouter des noms de zones source manuellement en cliquant sur une zone et en cliquant sur l'icône de mappage ![Icône de mappage](/images/MappingIcon.jpg). Vous pouvez également taper un texte ou utiliser une fonction de transformation pour personnaliser la valeur source. Pour plus d'informations, voir [How to use transformations ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://developer.ibm.com/integration/docs/app-connect/faq/#faq_transforms).
1. Facultatif : pour affiner le fonctionnement de votre flux, vous pouvez :
    * Ajouter des applications cible et des actions supplémentaires en cliquant sur l'icône + dans le flux ![Icône Ajouter une application](/images/AddApp.jpg).
    * Ajouter des actions d'extraction à votre flux pour extraire des éléments qui correspondent à certains critères, extraire un nombre spécifique d'enregistrements, définir la gestion des erreurs ou définir comment vous traitez les éléments extraits (voir [Using App Connect to retrieve items from your applications ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/using-ibm-app-connect-retrieve-items-applications/)).
    * Ajouter une logique conditionnelle pour effectuer des actions différentes en fonction des données reçues des applications dans votre flux (voir [Adding conditional logic to a flow ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/adding-conditional-logic-flow/)).

1. Une fois votre flux configuré, ouvrez le menu d'options sur la barre d'en-tête et cliquez sur **Start flow**.

Si vous retournez au tableau de bord d'{{site.data.keyword.appconserviceshort}}, vous pouvez voir votre flux s'exécuter. Lorsqu'un événement se produit dans la première application, une action est automatiquement déclenchée par {{site.data.keyword.appconserviceshort}} dans votre deuxième application. Vous pouvez voir l'état de vos flux sur le tableau de bord d'{{site.data.keyword.appconserviceshort}}. Pour afficher les journaux de vos flux, ouvrez le menu hamburger ![Icône du menu hamburger](/images/HamburgerMenuSm.jpg), développez **Manage**, puis cliquez sur **Logs**.

Pour en savoir plus sur la création des flux événementiels et obtenir des exemples, voir [Création d'un flux événementiel ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/creating-event-driven-flow/).

## Création d'un flux pour API

Si vous souhaitez qu'un développeur puisse créer une application qui utilise les données de vos applications basées sur le cloud, vous pouvez fournir une API. Pour créer des flux pour une API, procédez comme suit.
1. Sur le tableau de bord d'{{site.data.keyword.appconserviceshort}}, cliquez sur **New** > **Flows for an API**.
1. Entrez un nom pour votre API.
1. Entrez un nom pour votre modèle qui reflète le type d'objet avec lequel votre API travaillera, puis cliquez sur **Create model**.
1. Ajoutez les propriétés requises pour définir la structure de votre objet avec laquelle votre API travaillera.
    Par exemple, si votre API créera ou extraira un client, vous pouvez ajouter des propriétés appelées Customer_ID, First_Name, Last_Name et Email_Address. Vous pouvez taper le nom d'une propriété ou cliquer sur **Select properties from applications** pour sélectionner les propriétés d'une ou de plusieurs applications auxquelles vous êtes connecté.
1. Cliquez sur **Operations** pour définir comment l'API interagira avec l'objet et ajoutez les opérations dont vous avez besoin. 
1. Pour chaque opération, cliquez sur **Implement flow** pour créer un flux qui définit comment chaque opération fonctionnera. 
1. Ajoutez une ou plusieurs applications cible au flux, entre la demande et la réponse.
    Si vous souhaitez que votre flux effectue des actions différentes dans différentes conditions, vous pouvez également ajouter une logique conditionnelle (voir [Adding conditional logic to a flow ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/adding-conditional-logic-flow/)).
1. Cliquez sur **Response** dans le flux pour définir la réponse qui sera renvoyée lorsque l'opération aura été effectuée. Mappez les zones disponibles de votre application cible. 
1. Cliquez sur **Done** pour retourner à votre modèle.
1. Une fois que tous vos modèles et toutes vos opérations ont été définis, démarrez l'API en sélectionnant **Start API** dans le menu. 

Vous avez créé les flux pour votre API. Sur le tableau de bord d'{{site.data.keyword.appconserviceshort}}, les flux pour API sont identifiés par l'icône API. Vous pouvez les démarrer et les arrêter comme n'importe quel autre flux. Vous pouvez ouvrir une API lorsqu'elle est en cours d'exécution, mais vous devez l'arrêter pour pouvoir l'éditer.

Pour en savoir plus sur la création des flux pour API et obtenir des exemples, voir [Creating flows for an API  ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/creating-flows-api/).

Pour savoir comment tester votre API, voir [Exposing an App Connect flow through API Connect ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://developer.ibm.com/integration/blog/2017/08/29/exposing-app-connect-flow-api-connect/).


## Exécution d'une solution d'intégration IBM Integration Bus (bêta Enterprise)

Si vous voulez déployer des solutions d'intégration développées dans IBM Integration Bus ou App Connect Enterprise dans le cloud sans avoir à acquérir ou à maintenir une infrastructure informatique, vous pouvez importer un fichier BAR contenant tous les artefacts qui forment votre solution d'intégration, puis exécuter le contenu dans un serveur d'intégration dans App Connect. Pour télécharger un fichier BAR vers App Connect, vous devez avoir la version 10.0.0.4 d'IBM Integration Bus (ou une version ultérieure) ou App Connect Enterprise installée sur votre site. 

Pour exécuter vos solutions Integration Bus ou App Connect Enterprise dans App Connect, procédez comme suit.
1. Sur le tableau de bord d'{{site.data.keyword.appconserviceshort}}, cliquez sur **Nouveau** > **Importer un fichier BAR**.
1. Sélectionnez le fichier BAR que vous souhaitez importer, éditez le nom si vous le souhaitez, puis cliquez sur **Importer**.
    Si vous voyez une erreur d'authentification, vérifiez que votre fichier BAR est valide (voir [What makes a BAR file valid in App Connect? ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/what-makes-a-bar-file-valid-for-app-connect-app-connect-enterprise-beta)).
    Un serveur d'intégration est créé et une vignette est ajoutée est ajoutée au tableau de bord pour le représenter. L'état passe de "Préparation" à "Arrêté" lorsque le serveur d'intégration est prêt à être configuré et démarré. 
1. Cliquez sur la vignette pour ouvrir le serveur d'intégration.
1. Configurez le serveur d'intégration :
    * Ajoutez ou éditez une description de votre solution d'intégration.
    * Configurez l'authentification de base HTTPS (voir [Configuring HTTPS basic authentication ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/configuring-https-basic-authentication-app-connect-enterprise-beta)).
    * Ajoutez une règle pour pouvoir vous connecter à des systèmes sur site (voir [Configuring secure connectivity between integration servers on App Connect and on-premises systems ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/configuring-secure-connectivity-between-integration-servers-on-app-connect-and-on-premises-systems-app-connect-enterprise-beta)).
1. Facultatif : pour séparer vos traitement du flux de messages entre votre environnement sur site et App Connect, configurez des flux appelables. Pour ceci, ouvrez le menu hamburger ![Icône du menu hamburger](/images/HamburgerMenuSm.jpg), développez **Gérer** et sélectionnez **Flux appelables** (voir [Sharing message flow processing between App Connect and Integration Bus ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/sharing-message-flow-processing-between-app-connect-and-integration-bus-app-connect-enterprise-beta)).
1. Une fois la configuration terminée, retournez au tableau de bord d'App Connect et démarrez le serveur d'intégration en ouvrant le menu de la vignette et en cliquant sur **Démarrer**.

Lorsque votre serveur d'intégration est exécuté, vous pouvez voir et télécharger les journaux en ouvrant le serveur d'intégration et en cliquant sur **Télécharger les journaux** ou **Afficher les journaux**. Pour afficher les journaux, vous devez ajouter une règle de consignation à votre serveur d'intégration (voir [Viewing logs for your integration servers ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/viewing-logs-for-your-integration-servers-in-app-connect-enterprise-beta).)

Pour plus d'informations, voir [Running your Integration Bus solutions in App Connect ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan).
