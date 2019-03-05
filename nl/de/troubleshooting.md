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


# Fehlerbehebung bei IBM App Connect
{: #troubleshooting}

Sie können Protokolle in Kibana anzeigen, um Fehler bei {{site.data.keyword.appconservicefull}}-Abläufen und Integrationsservern zu beheben. Bei Fragen oder Problemen bei der Verwendung von {{site.data.keyword.appconserviceshort}} erhalten Sie Hilfe, indem Sie in einem Forum nach Informationen suchen oder Fragen stellen. Wenn Sie eine Frage über die Foren stellen, kennzeichnen Sie Ihre Frage so, dass sie von den {{site.data.keyword.Bluemix}}- und {{site.data.keyword.appconserviceshort}}-Entwicklerteams gesehen wird.

-   Sehen Sie sich die Kachel für einen aktiven Ablauf im {{site.data.keyword.appconserviceshort}}-Dashboard an. Wenn ein grünes Häkchen vorhanden ist, wurde der Ablauf erfolgreich ausgeführt. Klicken Sie auf das Häkchen, um zu sehen, wann der Ablauf zuletzt ausgelöst wurde.

    ![Screenshot mit einem erfolgreich ausgeführten Ablauf](/images/SuccessfulFlow.jpg)

    Wird ein rotes Ausrufezeichen angezeigt, liegt ein Problem vor. Klicken Sie auf das Ausrufezeichen um herauszufinden, worin der Fehler besteht. ![Screenshot mit einem Ablauf, der einen Fehler aufweist](/images/ErroredFlow.jpg)

-   Überprüfen Sie die {{site.data.keyword.appconserviceshort}}-Statusseite, um anzuzeigen, ob es aktuell bekannte Probleme gibt oder ob eine Wartung geplant ist: [{{site.data.keyword.appconserviceshort}}-Statusseite ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen  Link")](https://developer.ibm.com/integration/docs/app-connect/app-connect-status/)
-   Zur Anzeige von Protokolldaten für Ihre Abläufe klicken Sie im {{site.data.keyword.appconserviceshort}}-Hamburger-Menü auf **Protokolle**. Fehler und Informationsnachrichten für Ihre Abläufe werden standardmäßig in Kibana angezeigt, wo Sie Daten für einen bestimmten Zeitraum anzeigen können oder Filter verwenden, um bestimmte Typen von Informationen anzuzeigen. Zur Anzeige von Debugging-Informationen für Ihre Abläufe öffnen Sie das Menü auf einer Ablaufkachel im {{site.data.keyword.appconserviceshort}}-Dashboard und wählen dann **Debugprotokollierung aktivieren** aus. Sie müssen dann Ihren Ablauf erneut starten, damit die Debugprotokollierung beginnen kann. Beachten Sie, dass durch die Aktivierung der Debugprotokollierung Debugprotokolleinträge, die möglicherweise Nutzerdaten enthalten, für IBM Bediener sichtbar werden. Weitere Informationen zu Debugprotokollierung finden Sie im Lernprogramm über die Fehlerbehebung Ihrer Nachrichtenflüsse [Debugging your message flows in {{site.data.keyword.appconserviceshort}}](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/debugging-message-flows-ibm-app-connect/).  Weitere Informationen zu Kibana finden Sie in der [Dokumentation zu Kibana ![Symbol für externen Link ](../../icons/launch-glyph.svg "Symbol für externen Link")](https://www.elastic.co/guide/en/kibana/4.0/discover.html).
-   Zur Anzeige von Protokolldaten für Ihre Integrationsserver öffnen Sie einen Integrationsserver und klicken auf **Protokolle herunterladen** oder **Protokolle anzeigen**. Zur Anzeige von Protokollen für einen Integrationsserver Kibana müssen Sie dem Integrationsserver eine Protokollierungsrichtlinie zuordnen (siehe den Abschnitt zum Thema Anzeigen von Protokollen für Ihre Integrationsserver [Viewing logs for your integration servers ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/viewing-logs-for-your-integration-servers-in-app-connect-enterprise-beta)).
-   Suchen Sie Antworten auf allgemeine Fragen zu {{site.data.keyword.appconserviceshort}} im Abschnitt mit häufig gestellten Fragen [Frequently asked questions about {{site.data.keyword.appconserviceshort}} ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://developer.ibm.com/integration/docs/app-connect/faq/).
-   Befolgen Sie die schrittweisen Anweisungen zum Verbinden Ihrer Anwendung in den [Lernprogrammen für {{site.data.keyword.appconserviceshort}} ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/).
-   Wenn Sie technische Fragen zur Entwicklung oder Bereitstellung einer Anwendung mit {{site.data.keyword.appconserviceshort}} haben, posten Sie Ihre Frage auf [Stack Overflow ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](http://stackoverflow.com/search?q=app-connect+ibm-bluemix) und versehen Sie die Frage mit den Tags "ibm-bluemix" und "app-connect" (mit einem Bindestrich).
-   Bei Fragen zum Service und zu Anweisungen für erste Schritte verwenden Sie das Forum [IBM developerWorks&reg; dW Answers ![Symbol für externen  Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://developer.ibm.com/answers/topics/app_connect/?smartspace=bluemix). Fügen Sie die Tags "bluemix" und "app_connect" (mit einem Unterstrich) ein. 

    Weitere Informationen zur Verwendung von {{site.data.keyword.Bluemix}}-Supportmechanismen finden Sie im Hilfeabschnitt [Getting help ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://console.ng.bluemix.net/docs/support/index.html#getting-help).


