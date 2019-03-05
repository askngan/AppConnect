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


# Introduzione a IBM App Connect
{: #gettingStarted}

{{site.data.keyword.appconservicefull}} ti aiuta a connettere le tue applicazioni, dalle semplici interazioni trigger-azione alle integrazioni complesse. Puoi utilizzare {{site.data.keyword.appconserviceshort}} per creare flussi guidati dagli eventi oppure flussi per le API; in alternativa, puoi caricare ed eseguire le soluzioni di integrazione che crei in IBM Integration Bus senza che ti occorra acquisire e mantenere un'infrastruttura IT. Puoi visualizzare e amministrare tutte le tue integrazioni - server di integrazione, flussi guidati dagli eventi e flussi per le API - in una singola ubicazione nel dashboard {{site.data.keyword.appconserviceshort}}. 

Dopo che hai creato un'istanza del servizio {{site.data.keyword.appconserviceshort}}, puoi accedere a {{site.data.keyword.appconserviceshort}} dal dashboard {{site.data.keyword.Bluemix}}.

La seguente procedura fornisce informazioni sufficienti a consentirti di iniziare a lavorare con App Connect.  Per istruzioni più dettagliate, guide procedurali per specifiche applicazioni, esercitazioni e video, vedi il set completo di documentazione in [IBM App Connect ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://developer.ibm.com/integration/docs/app-connect/).

## Creazione di un flusso guidato dagli eventi

Come suggerito dal nome, un flusso guidato dagli eventi è formato da un evento in un'applicazione di origine che attiva il flusso e da una o più azioni nelle applicazioni di destinazione. Quindi, quando si verifica un evento nell'applicazione di origine, nelle tue applicazioni di destinazione viene attivata un'azione. Per creare un flusso guidato dagli eventi che connette le tue applicazioni basate sul cloud, completa la seguente procedura.
1.  Nel dashboard {{site.data.keyword.appconserviceshort}}, fai clic su **New** > **Event-driven flow**.
    {{site.data.keyword.appconserviceshort}} salva le tue modifiche automaticamente man mano che lavori. Se lo abbandoni a qualsiasi punto, il flusso viene salvato come una bozza di flusso che puoi completare in un secondo momento.
1.  Immetti un nome per il tuo flusso.
1.  Seleziona l'evento di trigger per avviare il tuo flusso espandendo un'applicazione e selezionando un evento.
1.  Se non sei già connesso alla tua applicazione, fai clic su **Connect to _applicazione_** e immetti i tuoi dettagli di accesso per l'applicazione.
    Potresti dover fornire dei dettagli di connessione aggiuntivi per qualche applicazione; sei hai bisogno di assistenza a trovare le credenziali per una specifica applicazione, consulta le guide procedurali per le applicazioni ([How-to guides for apps ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://developer.ibm.com/integration/docs/app-connect/how-to-guides-for-apps/)).
1.  Seleziona l'azione da attivare nella tua seconda applicazione espandendo un'applicazione e selezionando un'azione.
    Se necessario, fai clic su **Connect to application** e immetti i tuoi dettagli di accesso per l'applicazione di destinazione.
1. Immetti i dati che vuoi trasferire tra le tue applicazioni.
    Puoi aggiungere nomi campo di origine manualmente facendo clic in un campo e facendo quindi clic sull'icona di associazione ![Icona di associazione](/images/MappingIcon.jpg). Puoi anche immettere del testo o usare una funzione di trasformazione per personalizzare il valore di origine. Per ulteriori informazioni, vedi [How to use transformations ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://developer.ibm.com/integration/docs/app-connect/faq/#faq_transforms).
1. Facoltativo: puoi perfezionare la modalità di funzionamento del tuo flusso eseguendo le seguenti operazioni:
    * Aggiungi ulteriori applicazioni e azioni di destinazione facendo clic sull'icona di segno più nel flusso ![Icona di aggiunta di un'applicazione](/images/AddApp.jpg).
    * Aggiungi azioni retrieve al tuo flusso per richiamare gli elementi che corrispondono a specifici criteri, richiamare uno specifico numero di record, definire la gestione degli errori o definire come gestisci gli elementi che vengono richiamati (vedi [Using App Connect to retrieve items from your applications ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/using-ibm-app-connect-retrieve-items-applications/)).
    * Aggiungi della logica condizionale per eseguire azioni differenti a seconda dei dati ricevuti dalle applicazioni nel tuo flusso (vedi [Adding conditional logic to a flow ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/adding-conditional-logic-flow/)).

1. Dopo che hai configurato il tuo flusso, apri il menu delle opzioni nella barra intestazione e fai clic su **Start flow**.

Se ritorni al dashboard {{site.data.keyword.appconserviceshort}}, puoi vedere il tuo flusso in esecuzione. Quando si verifica un evento nella prima applicazione, {{site.data.keyword.appconserviceshort}} attiva automaticamente un'azione nella tua seconda applicazione. Puoi visualizzare lo stato dei tuoi flussi nel dashboard {{site.data.keyword.appconserviceshort}}. Per visualizzare i log per i tuoi flussi, apri il menu a tre linee ![Icona di menu a tre linee](/images/HamburgerMenuSm.jpg), espandi **Manage** e fai quindi clic su **Logs**.

Per informazioni più dettagliate sulla creazione di flussi guidati dagli eventi, compresi alcuni esempi, vedi [Creating an event-driven flow ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/creating-event-driven-flow/).

## Creazione di un flusso per un'API

Se vuoi che uno sviluppatore possa creare un'applicazione che utilizza i dati nelle tue applicazioni basate sul cloud, puoi fornire un'API. Per creare dei flussi per un'API, completa la seguente procedura.
1. Nel dashboard {{site.data.keyword.appconserviceshort}}, fai clic su **New** > **Flows for an API**.
1. Immetti un nome per la tua API.
1. Immetti un nome per il tuo modello che rifletta il tipo di oggetto con cui lavorerà la tua API e fai quindi clic su **Create model**.
1. Aggiungi le proprietà necessarie per definire la struttura del tuo oggetto con cui lavorerà la tua API.
    Ad esempio, se la tua API creerà o richiamerà un cliente, potresti aggiungere le proprietà denominate Customer_ID, First_Name, Last_Name e Email_Address. Puoi immettere il nome di una proprietà oppure fare clic su **Select properties from applications** per scegliere le proprietà da una o più applicazioni a cui sei connesso.
1. Fai clic su **Operations** per definire il modo in cui l'API interagirà con l'oggetto e aggiungere le operazioni di cui hai bisogno. 
1. Per ogni operazione, fai clic su **Implement flow** per creare un flusso che definisce come funzionerà ciascuna operazione. 
1. Aggiungi una o più applicazioni di destinazione al flusso, tra la richiesta e la risposta.
    Se vuoi che il tuo flusso esegua attività differenti per condizioni differenti, puoi anche aggiungere della logica condizionale (vedi [Adding conditional logic to a flow ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/adding-conditional-logic-flow/)).
1. Fai clic su **Response** nel flusso per definire la risposta che verrà restituita dopo che l'operazione sarà stata eseguita. Associa i campi disponibili dalla tua applicazione di destinazione. 
1. Fai clic su **Done** per ritornare al tuo modello.
1. Dopo che hai definito tutti i tuoi modelli e tutte le tue operazioni, avvia l'API selezionando **Start API** dal menu. 

Hai creato i flussi per la tua API. Nel dashboard {{site.data.keyword.appconserviceshort}}, i flussi per le API sono identificati dall'icona di API. Puoi avviarli e arrestarli nello stesso modo di qualsiasi altro flusso. Puoi aprire un'API mentre è in esecuzione ma devi arrestarla prima di poterla modificare.

Per informazioni più dettagliate sulla modalità di creazione dei flussi per le API, compresi degli esempi, vedi [Creating flows for an API  ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/creating-flows-api/).

Per informazioni su come eseguire un test della tua API, vedi [Exposing an App Connect flow through API Connect ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://developer.ibm.com/integration/blog/2017/08/29/exposing-app-connect-flow-api-connect/).


## Esecuzione di una soluzione di integrazione IBM Integration Bus (Enterprise beta)

Se vuoi distribuire delle soluzioni di integrazione che hai sviluppato in IBM Integration Bus o App Connect Enterprise al cloud, senza dover acquisire e mantenere un'infrastruttura IT, puoi importare un file BAR che contiene tutte le risorse utente che formano la tua soluzione di integrazione ed eseguire quindi il contenuto in un server di integrazione in App Connect. Per caricare un file BAR su App Connect, devi disporre di IBM Integration Bus versione 10.0.0.4 o successiva oppure di App Connect Enterprise installati in loco.

Per eseguire le tue soluzioni Integration Bus o App Connect Enterprise in App Connect, completa la seguente procedura:
1. Nel dashboard {{site.data.keyword.appconserviceshort}}, fai clic su **New** > **Import a BAR file**.
1. Seleziona il file BAR che vuoi importare, se lo desideri modificane il nome e fai quindi clic su **Import**.
    Se vedi un errore di autenticazione, controlla che il tuo file BAR sia valido (vedi [What makes a BAR file valid for App Connect? ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/what-makes-a-bar-file-valid-for-app-connect-app-connect-enterprise-beta)).
    Viene creato un server di integrazione e al dashboard viene aggiunto un tile per rappresentarlo. Lo stato cambierà da "Preparing" a "Stopped" quando il server di integrazione sarà pronto a essere configurato e avviato. 
1. Fai clic sul tile per aprire il server di integrazione.
1. Configura il server di integrazione:
    * Aggiungi o modifica una descrizione per la tua soluzione di integrazione.
    * Configura l'autenticazione di base HTTPS (vedi [Configuring HTTPS basic authentication ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/configuring-https-basic-authentication-app-connect-enterprise-beta)).
    * Collega una politica in modo che tu possa stabilire una connessione ai sistemi in loco (vedi [Configuring secure connectivity between integration servers on App Connect and on-premises systems ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/configuring-secure-connectivity-between-integration-servers-on-app-connect-and-on-premises-systems-app-connect-enterprise-beta)).
1. Facoltativo: per suddividere l'elaborazione del flusso di messaggi tra il tuo ambiente in loco e App Connect, configura dei flussi richiamabili aprendo il menu a tre linee ![Icona di menu a tre linee](/images/HamburgerMenuSm.jpg), espandendo **Manage** e selezionando **Callable flows** (vedi [Sharing message flow processing between App Connect and Integration Bus ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/sharing-message-flow-processing-between-app-connect-and-integration-bus-app-connect-enterprise-beta)).
1. Dopo che hai completato la configurazione, ritorna al dashboard App Connect e avvia il server di integrazione aprendo il menu del tile e facendo clic su **Start**.

Una volta che il tuo server di integrazione è in esecuzione, puoi visualizzare e scaricare i log aprendo il server di integrazione e facendo clic su **Download logs** o **View logs**. Per visualizzare i log, devi collegare una politica di registrazione in log al tuo server di integrazione (vedi [Viewing logs for your integration servers ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/viewing-logs-for-your-integration-servers-in-app-connect-enterprise-beta).)

Per informazioni più dettagliate, vedi [Running your Integration Bus solutions in App Connect ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan).
