---

copyright:
  years: 2017
lastupdated: "2018-07-20"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip} 
{:download: .download}


# Einführung in IBM App Connect
{: #gettingStarted}

{{site.data.keyword.appconservicefull}} hilft Ihnen dabei, Ihre Anwendungen zu verbinden: von einfachen Interaktionen mit Auslöseraktionen bis hin zu komplexen Integrationen. Sie können {{site.data.keyword.appconserviceshort}} verwenden, um ereignisgesteuerte Abläufe oder Abläufe für APIs zu erstellen. Sie können die von Ihnen in IBM Integration Bus erstellten Integrationslösungen auch hochladen und ausführen, ohne eine IT-Infrastruktur anzufordern oder warten zu müssen. Sie können alle Ihre Integrationen wie Integrationsserver, ereignisgesteuerte Abläufe und Abläufe für APIs an einem Ort, nämlich im {{site.data.keyword.appconserviceshort}}-Dashboard anzeigen und verwalten. 

Nachdem Sie eine Instanz des {{site.data.keyword.appconserviceshort}}-Service erstellt haben, können Sie vom {{site.data.keyword.Bluemix}}-Dashboard auf {{site.data.keyword.appconserviceshort}} zugreifen. 

Die folgenden Schritte bieten Ihnen genügend Informationen für den Start mit App Connect. Ausführlichere Anweisungen, Verwendungshinweise für bestimmte Anwendungen und Videos finden Sie in der gesamten Reihe der Dokumentation unter [IBM App Connect ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://developer.ibm.com/integration/docs/app-connect/).

## Ereignisgesteuerten Ablauf erstellen

Wie der Name bereits vermuten lässt, besteht ein ereignisgesteuerter Ablauf aus einem Ereignis in einer Quellenanwendung, das den Ablauf auslöst, und einer oder mehreren Aktionen in Zielanwendungen. Wenn ein Ereignis in der Quellenanwendung auftritt, wird eine Aktion in Ihrer Zielanwendung ausgelöst. Führen Sie die folgenden Schritte aus, um einen ereignisgesteuerten Ablauf zu erstellen, der Ihre cloudbasierten Anwendungen verbindet. 
1.  Klicken Sie im {{site.data.keyword.appconserviceshort}}-Dashboard auf **Neu** > **Ereignisgesteuerter Ablauf**.
    {{site.data.keyword.appconserviceshort}} speichert Ihre Änderungen automatisch. Wenn Sie den Ablauf in einem beliebigen Stadium verlassen, wird der Ablauf als Entwurf gespeichert, den Sie zu einem späteren Zeitpunkt vervollständigen können. 
1.  Geben Sie einen Namen für Ihren Ablauf ein. 
1.  Wählen Sie eine Ereignisbedingung aus, um Ihren Ablauf zu starten, indem Sie eine Anwendung einblenden und ein Ereignis auswählen. 
1.  Wenn Sie noch keine Verbindung zu Ihrer Anwendung hergestellt haben, klicken Sie auf **Verbinden mit _anwendung_** und geben Sie Ihre Anmeldedetails für die Anwendung ein.
    Möglicherweise müssen Sie zusätzliche Verbindungsdetails für einige Anwendungen bereitstellen. Wenn Sie Hilfe beim Suchen der Berechtigungsnachweise für eine bestimmte Anwendung benötigen, sehen Sie in den Verwendungshinweisen für Apps [How-to guides for apps ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://developer.ibm.com/integration/docs/app-connect/how-to-guides-for-apps/) nach.
1.  Wählen Sie eine Aktion aus, die in Ihrer zweiten Anwendung ausgelöst werden soll, indem Sie eine Anwendung einblenden und eine Aktion auswählen. Bei Bedarf klicken Sie auf **Mit Anwendung verbinden** und geben Ihre Anmeldedetails für die Zielanwendung ein. 
1. Geben Sie die Daten ein, die Sie zwischen Ihren Anwendungen übertragen möchten. Sie können Quellenfeldnamen manuell hinzufügen oder durch Klicken in ein Feld und anschließendes Klicken auf das Zuordnungssymbol ![Zuordnungssymbol](/images/MappingIcon.jpg). Sie können ferner in einen Text schreiben oder eine Transformationsfunktion zum Anpassen des Quellenwerts verwenden. Weitere Informationen finden Sie in den Verwendungshinweisen für Transformationen [How to use transformations ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://developer.ibm.com/integration/docs/app-connect/faq/#faq_transforms).
1. Optional: Sie können die Funktionsweise des Ablaufs optimieren, indem Sie die folgenden Schritte ausführen:
    * Fügen Sie weitere Zielanwendungen und Aktionen hinzu, indem Sie auf das Pluszeichen im Ablauf ![Symbol 'Anwendung hinzufügen'](/images/AddApp.jpg) klicken.
    * Fügen Sie Abrufaktionen zu Ihrem Ablauf hinzu, um Elemente abzurufen, die bestimmten Kriterien entsprechen, um eine bestimmte Anzahl an Datensätzen abzurufen, die Fehlerbehandlung zu definieren oder um zu definieren, wie die abgerufenen Elemente verarbeitet werden sollen (siehe den Abschnitt zur Verwendung von App Connect zum Abrufen von Elementen von Ihren Anwendungen [Using App Connect to retrieve items from your applications ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/using-ibm-app-connect-retrieve-items-applications/)).
    * Fügen Sie Bedingungslogik hinzu, um abhängig von den Daten, die von den Anwendungen im Ablauf empfangen werden, unterschiedliche Aktionen auszuführen (siehe den Abschnitt über das Hinzufügen von Bedingungslogik zu einem Ablauf [Adding conditional logic to a flow ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/adding-conditional-logic-flow/)).

1. Wenn Sie Ihren Ablauf konfiguriert haben, öffnen Sie das Auswahlmenü in der Titelleiste und klicken auf **Ablauf starten**.

Wenn Sie zum {{site.data.keyword.appconserviceshort}}-Dashboard zurückkehren, können Sie die Ausführung Ihres Ablaufs sehen. Wenn ein Ereignis in der ersten Anwendung auftritt, wird von {{site.data.keyword.appconserviceshort}} automatisch eine Aktion in der zweiten Anwendung ausgelöst. Sie können den Status Ihrer Abläufe im {{site.data.keyword.appconserviceshort}}-Dashboard ansehen. Wenn Sie Protokolle für Ihre Abläufe anzeigen möchten, öffnen Sie das Hamburger-Menü ![Symbol 'Hamburger-Menü'](/images/HamburgerMenuSm.jpg), blenden **Verwalten** ein und klicken dann auf **Protokolle**.

Ausführlichere Informationen zum Erstellen von ereignisgesteuerten Abläufen einschließlich einiger Beispiele finden Sie im Abschnitt zum Erstellen eines ereignisgesteuerten Ablaufs [Creating an event-driven flow ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/creating-event-driven-flow/).

## Ablauf für eine API erstellen

Wenn Sie möchten, dass ein Entwickler eine Anwendung erstellen kann, die die Daten in Ihren cloudbasierten Anwendungen verwendet, können Sie ein API bereitstellen. Führen Sie die folgenden Schritte aus, um Abläufe für eine API zu erstellen. 
1. Klicken Sie im {{site.data.keyword.appconserviceshort}}-Dashboard auf **Neu** > **Abläufe für eine API**.
1. Geben Sie den Namen für Ihre API ein. 
1. Geben Sie einen Namen für Ihr Modell ein, das den Objekttyp widerspiegelt, mit dem Ihre API arbeiten wird, und klicken Sie dann auf **Modell erstellen**.
1. Fügen Sie die für die Definition der Objektstruktur erforderlichen Eigenschaften für das Objekt hinzu, mit dem Ihre API arbeiten wird. Wenn Ihre API beispielsweise einen Kunden erstellen oder abrufen soll, können Sie Eigenschaften wie 'Customer_ID', 'First_Name', 'Last_Name' und 'Email_Address' hinzufügen. Sie können entweder den Namen einer Eigenschaft eingeben oder auf **Eigenschaften aus Anwendungen auswählen** klicken, um Eigenschaften aus einer oder mehreren der Anwendungen auszuwählen, mit denen Sie verbunden sind.
1. Klicken Sie auf **Operationen**, um zu definieren, wie die API mit dem Objekt interagieren soll, und fügen Sie die benötigten Operationen hinzu. 
1. Klicken Sie für jede Operation auf **Ablauf implementieren**, um einen Ablauf zu erstellen, der definiert, wie die einzelnen Operationen funktionieren. 
1. Fügen Sie mindestens eine Zielanwendung zwischen der Anforderung und der Antwort zum Ablauf hinzu. Wenn der Ablauf bei unterschiedlichen Bedingungen andere Aktionen ausführen soll, können Sie Bedingungslogik hinzufügen (siehe den Abschnitt zum Hinzufügen von Bedingungslogik zu einem Ablauf [Adding conditional logic to a flow ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/adding-conditional-logic-flow/)).
1. Klicken Sie im Ablauf auf die **Antwort**, die zurückgegeben wird, wenn die Operation ausgeführt worden ist. Ordnen Sie die verfügbaren Felder von Ihrer Zielanwendung zu.  
1. Klicken Sie auf **Fertig**, um zu Ihrem Modell zurückzukehren. 
1. Wenn Sie alle Modelle und Operationen definiert haben, starten Sie die API, indem Sie im Menü **API starten** auswählen.  

Sie haben die Abläufe für Ihre API erstellt. Im {{site.data.keyword.appconserviceshort}}-Dashboard werden Abläufe für APIs durch das API-Symbol gekennzeichnet. Sie können APIs ebenso wie jeden anderen Ablauf starten und stoppen. Sie können eine API öffnen, während diese aktiv ist, aber Sie müssen Sie stoppen, wenn Sie sie bearbeiten möchten. 

Ausführlichere Informationen zur Vorgehensweise bei der Erstellung von Abläufen für APIs sowie Bespiele dazu finden Sie im Abschnitt zum Erstellen von Abläufen für eine API [Creating flows for an API  ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/creating-flows-api/).

Um herauszufinden, wie Sie Ihre API testen können, lesen Sie den Abschnitt über das Offenlegen eines App Connect-Ablaufs über API Connect [Exposing an App Connect flow through API Connect ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://developer.ibm.com/integration/blog/2017/08/29/exposing-app-connect-flow-api-connect/).


## Eine IBM Integration Bus-Integrationslösung (Enterprise Betaversion) ausführen

Wenn Sie Integrationslösungen bereitstellen möchten, die Sie in IBM Integration Bus oder App Connect Enterprise für die Cloud entwickelt haben, ohne eine IT-Infrastruktur anfordern oder warten zu müssen, können Sie ein BAR-Datei importieren, die alle Artefakte Ihrer Integrationslösung enthält, und dann den Inhalt auf einem Integrationsserver in App Connect ausführen. Zum Hochladen einer BAR-Datei in App Connect müssen Sie über lokale Installationen von IBM Integration Bus Version 10.0.0.4 oder höher oder über App Connect Enterprise verfügen. 

Führen Sie die folgenden Schritte aus, um Ihre Integration Bus- oder App Connect Enterprise-Lösungen in App Connect auszuführen. 
1. Klicken Sie im {{site.data.keyword.appconserviceshort}}-Dashboard auf **Neu** > **BAR-Datei importieren**.
1. Wählen Sie die gewünschte BAR-Datei für den Import aus, bearbeiten Sie bei Bedarf den Namen und klicken Sie dann auf **Importieren**.
    Wenn ein Authentifizierungsfehler angezeigt wird, überprüfen Sie, dass die BAR-Datei gültig ist (siehe den Abschnitt über die Gültigkeit von BAR-Dateien in App Connect [What makes a BAR file valid in App Connect? ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/what-makes-a-bar-file-valid-for-app-connect-app-connect-enterprise-beta)).
Ein Integrationsserver wird erstellt und durch eine neu hinzugefügte Kachel im Dashboard dargestellt. Der Status ändert sich von "Preparing" (in Vorbereitung) in "Stopped" (Gestoppt), wenn der Integrationsserver bereit ist, konfiguriert und gestartet zu werden.  
1. Klicken Sie auf die Kachel, um den Integrationsserver zu öffnen.
1. Konfigurieren Sie den Integrationsserver: 
    * Fügen Sie eine Beschreibung für Ihre Integrationslösung hinzu oder bearbeiten Sie eine vorhandene Beschreibung. 
    * Konfigurieren Sie die HTTPS-Basisauthentifizierung (siehe den Abschnitt über die Konfiguration der HTTPS-Basisauthentifizierung [Configuring HTTPS basic authentication ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/configuring-https-basic-authentication-app-connect-enterprise-beta)).
    * Ordnen Sie ein Richtlinie hinzu, damit die Verbindung zu lokalen Systemen hergestellt werden kann (siehe den Abschnitt über die Konfiguration der Sicherheitskonnektivität zwischen Integrationsservern unter App Connect und lokalen Systemen [Configuring secure connectivity between integration servers on App Connect and on-premises systems ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/configuring-secure-connectivity-between-integration-servers-on-app-connect-and-on-premises-systems-app-connect-enterprise-beta)).
1. Optional: Um die Verarbeitung des Nachrichtenflusses zwischen Ihrer lokalen Umgebung und App Connect aufzuteilen, konfigurieren Sie aufrufbare Abläufe, indem Sie das Hamburger-Menü ![Symbol für Hamburger-Menü](/images/HamburgerMenuSm.jpg) öffnen, das Element **Verwalten** einblenden und **Aufrufbare Abläufe** auswählen (siehe den Abschnitt zur gemeinsamen Verarbeitung des Nachrichtenflusses durch App Connect und Integration Bus [Sharing message flow processing between App Connect and Integration Bus ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/sharing-message-flow-processing-between-app-connect-and-integration-bus-app-connect-enterprise-beta)).
1. Wenn Sie die Konfiguration abgeschlossen haben, kehren Sie zum App Connect-Dashboard zurück und starten den Integrationsserver, indem Sie das Kachelmenü öffnen und auf **Starten** klicken.

Wenn der Integrationsserver aktiv ist, können Sie Protokolle anzeigen und herunterladen, indem Sie den Integrationsserver öffnen und auf **Protokolle herunterladen** oder **Protokolle anzeigen** klicken. Zur Anzeige der Protokolle müssen Sie Ihrem Integrationsserver eine Protokollierungsrichtlinie zuordnen (siehe den Abschnitt über das Anzeigen von Protokollen für Ihre Integrationsserver [Viewing logs for your integration servers ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/viewing-logs-for-your-integration-servers-in-app-connect-enterprise-beta).)

Ausführlichere Informationen finden Sie im Abschnitt über die Ausführung Ihrer Integration Bus-Lösungen in App Connect [Running your Integration Bus solutions in App Connect ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan).
