---

copyright:
  years: 2017, 2019
lastupdated: "2019-08-14"

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

-   Observez la vignette d'un flux en cours sur le tableau de bord d'{{site.data.keyword.appconserviceshort}}. Si vous voyez une coche verte, le flux s'exécute correctement ; cliquez sur la coche pour voir quand le flux a été déclenché pour la dernière fois.

    ![Capture d'écran montrant qu'un flux est en cours d'exécution](/images/SuccessfulFlow.jpg)

    Si un point d'exclamation rouge apparaît, cela signifie qu'un problème s'est produit ; cliquez sur le point d'exclamation pour connaître les détails de l'incident. ![Capture d'écran montrant qu'un problème s'est produit sur un flux](/images/ErroredFlow.jpg)

-   Consultez la page d'état d'{{site.data.keyword.appconserviceshort}} pour voir si des problèmes sont signalés ou si la maintenance est planifiée : [page d'état {{site.data.keyword.appconserviceshort}} ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://developer.ibm.com/integration/docs/app-connect/app-connect-status/) 
-   Pour afficher les informations de journal de vos flux, cliquez sur **Journaux** dans le menu d'{{site.data.keyword.appconserviceshort}}. Les messages d'erreur et d'information de vos flux sont affichés par défaut dans Kibana, où vous pouvez visualiser les données pour une plage de temps spécifique, ou utiliser des filtres pour afficher certains types d'informations. Pour afficher les informations de débogage de vos flux, ouvrez le menu d'une vignette de flux sur le tableau de bord d'{{site.data.keyword.appconserviceshort}}, puis sélectionnez **Activer la consignation du débogage**.  Vous devez ensuite redémarrer votre flux pour que la consignation du débogage puisse commencer. Lorsque vous activez la consignation du débogage, les entrées du journal de débogage, y compris éventuellement les données utiles, sont visibles par les opérateurs IBM. Pour en savoir plus sur la consignation du débogage, voir [Déboguge de vos flux de messages dans {{site.data.keyword.appconserviceshort}} ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/debugging-message-flows-ibm-app-connect/).  Pour en savoir plus sur Kibana, voir la [documentation de Kibana ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://www.elastic.co/guide/en/kibana/4.0/discover.html).
-   Pour afficher les informations de journal de vos serveurs d'intégration, ouvrez un serveur d'intégration et cliquez sur **Télécharger les journaux** ou **Afficher les journaux**. Pour afficher les journaux d'un serveur d'intégration dans Kibana, vous devez associer une règle de consignation à ce serveur d'intégration (voir [Affichage des journaux pour vos serveurs d'intégration ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/viewing-logs-for-your-integration-servers-in-app-connect-enterprise-beta)).
-   Trouvez les réponses aux questions fréquemment posées sur {{site.data.keyword.appconserviceshort}} dans [Frequently asked questions about {{site.data.keyword.appconserviceshort}} ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://developer.ibm.com/integration/docs/app-connect/faq/).
-   Suivez les instructions étape par étape sur la façon de connecter vos applications dans [Tutorials for {{site.data.keyword.appconserviceshort}} ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/).
-   Pour toute question sur le service et la mise en route, utilisez le forum  [IBM dW Answers ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://developer.ibm.com/answers/topics/app_connect). Incluez les balises "ibm_cloud" et "app_connect" (avec un trait de soulignement).

    Pour en savoir plus sur l'utilisation des mécanismes de support de {{site.data.keyword.Bluemix}}, voir [Support ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://cloud.ibm.com/unifiedsupport/supportcenter).

## Signalement d'un problème à l'équipe IBM App Connect 
{: #reporting}

Si vous avez suivi le conseil de traitement des incidents et que le problème persiste, vous pouvez obtenir de l'aide auprès de l'équipe {{site.data.keyword.appconserviceshort}}. Dans le menu {{site.data.keyword.appconserviceshort}}, cliquez sur **Nous contacter**, puis sur **Support technique**. Connectez-vous avec votre ID IBM, cliquez sur **Créer un cas**, et fournissez autant d'informations que possible. (Vous pouvez également cliquer sur **Support** dans la console {{site.data.keyword.Bluemix}}.) 

* Région {{site.data.keyword.Bluemix}} où votre instance d'{{site.data.keyword.appconserviceshort}} est mise à disposition. (Par exemple, Dallas ou Londres.)
* ID d'instance du service {{site.data.keyword.appconserviceshort}} que vous utilisez. (Vous pouvez trouver cet ID en consultant les informations du compte sous l'identificateur d'instance {{site.data.keyword.appconserviceshort}}.)
* Problème que vous rencontrez. (Par exemple, si le problème concerne une application ou une fonction spécifique.) 
* ID de lot si le problème est lié au traitement par lot. (Si des erreurs se produisent dans un processus de traitement par lots et que vous avez défini un ID pour chaque enregistrement du processus de traitement par lots, vous pouvez trouver votre ID défini dans la colonne "batch-record-id_str" du journal Kibana. Voir [Comment utiliser le traitement par lots dans {{site.data.keyword.appconserviceshort}} ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://developer.ibm.com/integration/docs/app-connect/toolbox-utilities/how-to-use-batch-processing-in-ibm-app-connect/).)
* Date et heure (y compris le fuseau horaire) à l'origine du problème et durée d'exécution du flux avant que le problème ne survienne. 
* Si le problème persiste et si vous pouvez le répliquer. 
* Le cas échéant, type de navigateur et version que vous utilisez. (Nous ne prenons en charge que les dernières versions du navigateur.) 
* Toutes les entrées de journal décrivant le problème. 
* Impact que le problème produit sur votre entreprise. 
