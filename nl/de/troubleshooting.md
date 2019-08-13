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


# Fehlerbehebung bei IBM App Connect
{: #troubleshooting}

Sie können Protokolle in Kibana anzeigen, um Fehler bei {{site.data.keyword.appconservicefull}}-Abläufen und Integrationsservern zu beheben. Bei Fragen oder Problemen bei der Verwendung von {{site.data.keyword.appconserviceshort}} erhalten Sie Hilfe, indem Sie in einem Forum nach Informationen suchen oder Fragen stellen. Wenn Sie eine Frage über die Foren stellen, kennzeichnen Sie Ihre Frage so, dass sie von den {{site.data.keyword.Bluemix}}- und {{site.data.keyword.appconserviceshort}}-Entwicklerteams gesehen wird.

-   Sehen Sie sich die Kachel für einen aktiven Ablauf im {{site.data.keyword.appconserviceshort}}-Dashboard an. Wenn ein grünes Häkchen vorhanden ist, wird der Ablauf erfolgreich ausgeführt. Klicken Sie auf das Häkchen, um zu sehen, wann der Ablauf zuletzt ausgelöst wurde.

    ![Screenshot, der anzeigt, dass ein Ablauf erfolgreich ausgeführt wird](/images/SuccessfulFlow.jpg)

    Wird ein rotes Ausrufezeichen angezeigt, liegt ein Problem vor. Klicken Sie auf das Ausrufezeichen, um herauszufinden, was das Problem ist. ![Screenshot, der anzeigt, dass bei einem Ablauf ein Problem vorliegt](/images/ErroredFlow.jpg)

-   Überprüfen Sie die {{site.data.keyword.appconserviceshort}}-Statusseite, um festzustellen, ob Probleme gemeldet wurden oder eine Wartung geplant ist: [{{site.data.keyword.appconserviceshort}}-Statusseite ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://developer.ibm.com/integration/docs/app-connect/app-connect-status/)
-   Zum Anzeigen von Protokolldaten für Ihre Abläufe klicken Sie auf **Protokolle** im {{site.data.keyword.appconserviceshort}}-Menü. Fehler und Informationsnachrichten für Ihre Abläufe werden standardmäßig in Kibana angezeigt, wo Sie Daten für einen bestimmten Zeitraum anzeigen können oder Filter verwenden, um bestimmte Typen von Informationen anzuzeigen. Zur Anzeige von Debugging-Informationen für Ihre Abläufe öffnen Sie das Menü auf einer Ablaufkachel im {{site.data.keyword.appconserviceshort}}-Dashboard und wählen dann **Debugprotokollierung aktivieren** aus.  Sie müssen dann Ihren Ablauf erneut starten, damit die Debugprotokollierung beginnen kann. Wenn Sie die Debugprotokollierung aktivieren, werden Debugprotokolleinträge, die möglicherweise Nutzdaten enthalten, für IBM Bediener sichtbar. Weitere Informationen zur Debugprotokollierung finden Sie unter  [Debugging von Nachrichtenflüssen in {{site.data.keyword.appconserviceshort}} ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/debugging-message-flows-ibm-app-connect/).  Weitere Informationen zu Kibana finden Sie in der [Dokumentation zu Kibana ![Symbol für externen Link ](../../icons/launch-glyph.svg "Symbol für externen Link")](https://www.elastic.co/guide/en/kibana/4.0/discover.html).
-   Zur Anzeige von Protokolldaten für Ihre Integrationsserver öffnen Sie einen Integrationsserver und klicken auf **Protokolle herunterladen** oder **Protokolle anzeigen**.  Zum Anzeigen von Protokollen für einen Integrationsserver in Kibana müssen Sie dem Integrationsserver eine Protokollierungsrichtlinie zuordnen (siehe [Protokolle für Ihre Integrationsserver anzeigen ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/viewing-logs-for-your-integration-servers-in-app-connect-enterprise-beta)).
-   Suchen Sie Antworten auf allgemeine Fragen zu {{site.data.keyword.appconserviceshort}} im Abschnitt mit häufig gestellten Fragen [Frequently asked questions about {{site.data.keyword.appconserviceshort}} ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://developer.ibm.com/integration/docs/app-connect/faq/).
-   Befolgen Sie die schrittweisen Anweisungen zum Verbinden Ihrer Anwendung in den [Lernprogrammen für {{site.data.keyword.appconserviceshort}} ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/).
-   Bei Fragen zum Service und zu den Anweisungen für erste Schritte verwenden Sie das Forum [IBM dW Answers ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://developer.ibm.com/answers/topics/app_connect). Verwenden Sie die Tags 'ibm_cloud' und 'app_connect' (mit einem Unterstrich). 

    Weitere Informationen zur Verwendung von {{site.data.keyword.Bluemix}}-Supportverfahren finden Sie unter [Support ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://cloud.ibm.com/unifiedsupport/supportcenter).

## Problem dem IBM App Connect-Team melden
{: #reporting}

Wenn Sie den Hinweisen zur Fehlerbehebung gefolgt sind und das Problem weiterhin besteht, können Sie Hilfe beim {{site.data.keyword.appconserviceshort}}-Team anfordern.  Klicken Sie im {{site.data.keyword.appconserviceshort}}-Menü auf **Kontaktaufnahme** und dann auf **Unterstützung anfordern**.  Melden Sie sich mit Ihrer IBM ID an, klicken Sie auf **Fall erstellen** und geben von den folgenden Informationen so viele wie möglich an. (Sie können auch auf **Support** in der {{site.data.keyword.Bluemix}}-Konsole klicken.) 

* Die {{site.data.keyword.Bluemix}}-Region, in der Ihre Instanz von {{site.data.keyword.appconserviceshort}} bereitgestellt wird. (Zum Beispiel Dallas oder London.)
* Die Instanz-ID des {{site.data.keyword.appconserviceshort}}-Service, den Sie verwenden. (Diese ID finden Sie in den Kontoinformationen unter der {{site.data.keyword.appconserviceshort}}-ID.)
* Ihr aktuelles Problem. (Zum Beispiel, ob das Problem bei einer bestimmten Anwendung oder Funktion auftritt.)
* Die Stapel-ID, wenn das Problem im Zusammenhang mit einer Stapelverarbeitung steht. (Wenn Fehler in einem Stapelprozess auftreten und Sie für jeden Datensatz in diesem Prozess eine ID definiert haben, steht Ihre definierte ID in der Spalte 'batch-record-id_str' des Kibana-Protokolls; siehe [Verwendung der Stapelverarbeitung in {{site.data.keyword.appconserviceshort}} ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://developer.ibm.com/integration/docs/app-connect/toolbox-utilities/how-to-use-batch-processing-in-ibm-app-connect/).)
* Das Datum und die Uhrzeit (einschließlich der Zeitzone) des ersten Auftretens des Problems sowie die Zeitdauer, die der Ablauf bis zum Auftreten des Problems ausgeführt wurde.
* Ob das Problem weiterhin auftritt und ob Sie es reproduzieren können.
* Falls zutreffend, der Typ und die Version des von Ihnen verwendeten Browsers. (Wir unterstützen nur die neuesten Browser-Versionen.)
* Alle Protokolleinträge, die das Problem beschreiben.
* Die Auswirkungen, die das Problem auf Ihr Unternehmen hat.
