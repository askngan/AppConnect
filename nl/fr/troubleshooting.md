---

copyright:
  years: 2017
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


# Traitement des incidents dans IBM App Connect
{: #troubleshooting}

Pour résoudre les problèmes liés aux flux et serveurs d'intégration d'{{site.data.keyword.appconservicefull}}, vous pouvez afficher les journaux dans Kibana. Si vous avez des questions ou des problèmes lorsque vous utilisez {{site.data.keyword.appconserviceshort}}, obtenez de l'aide en recherchant des informations ou en posant des questions sur un forum. Lorsque vous utilisez les forums pour poser une question, identifiez votre question de façon à ce qu'elle soit vue par les équipes de développement de {{site.data.keyword.Bluemix}} et {{site.data.keyword.appconserviceshort}}.

-   Observez la vignette d'un flux en cours sur le tableau de bord d'{{site.data.keyword.appconserviceshort}}. Si vous voyez une coche verte, le flux s'est exécuté correctement ; cliquez sur la coche pour voir quand le flux a été déclenché pour la dernière fois.

    ![Capture d'écran montrant qu'un flux s'est exécuté correctement](/images/SuccessfulFlow.jpg)

    S'il y a un point d'exclamation rouge, il y a un problème ; cliquez sur le point d'exclamation pour connaître les détails de l'incident. ![Capture d'écran montrant qu'un flux a un problème](/images/ErroredFlow.jpg)

-   Consultez la page d'état {{site.data.keyword.appconserviceshort}} pour voir s'il y a des problèmes actuels connus ou si une maintenance est prévue : [Page d'état d'{{site.data.keyword.appconserviceshort}} ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://developer.ibm.com/integration/docs/app-connect/app-connect-status/)
-   Pour afficher les informations de journal de vos flux, cliquez sur **Journaux** dans le menu hamburger d'{{site.data.keyword.appconserviceshort}}. Les messages d'erreur et d'information de vos flux sont affichés par défaut dans Kibana, où vous pouvez visualiser les données pour une plage de temps spécifique, ou utiliser des filtres pour afficher certains types d'informations. Pour afficher les informations de débogage de vos flux, ouvrez le menu d'une vignette de flux sur le tableau de bord d'{{site.data.keyword.appconserviceshort}}, puis sélectionnez **Activer la consignation du débogage**. Vous devrez ensuite redémarrer votre flux pour que la consignation du débogage puisse commencer. Notez que lorsque vous activez la consignation du débogage, les entrées du journal de débogage, y compris éventuellement les données utiles, sont visibles par les opérateurs IBM. Pour en savoir plus sur la consignation du débogage, voir [Debugging your message flows in {{site.data.keyword.appconserviceshort}}](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/debugging-message-flows-ibm-app-connect/). Pour en savoir plus sur Kibana, voir la [documentation de Kibana ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://www.elastic.co/guide/en/kibana/4.0/discover.html).
-   Pour afficher les informations de journal de vos serveurs d'intégration, ouvrez un serveur d'intégration et cliquez sur **Télécharger les journaux** ou **Afficher les journaux**. Pour afficher les journaux d'un serveur d'intégration dans Kibana, vous devez associer une règle de consignation à ce serveur d'intégration (voir [Viewing logs for your integration servers ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/viewing-logs-for-your-integration-servers-in-app-connect-enterprise-beta)).
-   Trouvez les réponses aux questions fréquemment posées sur {{site.data.keyword.appconserviceshort}} dans [Frequently asked questions about {{site.data.keyword.appconserviceshort}} ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://developer.ibm.com/integration/docs/app-connect/faq/).
-   Suivez les instructions étape par étape sur la façon de connecter vos applications dans [Tutorials for {{site.data.keyword.appconserviceshort}} ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/).
-   Si vous avez des questions techniques sur le développement ou le déploiement d'une application avec {{site.data.keyword.appconserviceshort}}, postez votre question sur [Stack Overflow ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](http://stackoverflow.com/search?q=app-connect+ibm-bluemix) et balisez votre question avec "ibm-bluemix" et "app-connect" (avec un tiret).
-   Pour toute question sur le service et la mise en route, utilisez le forum [IBM developerWorks&reg; dW Answers ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://developer.ibm.com/answers/topics/app_connect/?smartspace=bluemix). Incluez les balises "bluemix" et "app_connect" (avec un trait de soulignement).

    Pour en savoir plus sur l'utilisation des mécanismes de support de {{site.data.keyword.Bluemix}}, voir [Obtenir de l'aide ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://console.ng.bluemix.net/docs/support/index.html#getting-help).


