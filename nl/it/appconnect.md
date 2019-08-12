---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-20"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip} 
{:download: .download}


# Concetti di IBM App Connect
{: #concepts}

{{site.data.keyword.appconservicefull}} è uno strumento ottimizzato per il business che puoi usare per integrare le tue applicazioni basate sul cloud o in loco per automatizzare attività tediose e ripetitive.

{{site.data.keyword.appconserviceshort}} connette le tue applicazioni nel giro di pochi minuti, automatizzando gli aggiornamenti, le notifiche e gli eventi e mantenendo i tuoi dati sincronizzati tra più applicazioni. Puoi utilizzarlo per connettere applicazioni nel cloud oppure applicazioni locali (in loco).  

Puoi eseguire due tipi di risorsa in {{site.data.keyword.appconserviceshort}} per connettere le tue applicazioni, a seconda delle tue esigenze di business: flussi e server di integrazione. Per eseguire le tue soluzioni IBM Integration Bus o App Connect Enterprise, carichi una soluzione di integrazione in un file BAR e lo esegui quindi in un server di integrazione in {{site.data.keyword.appconserviceshort}}. Crei i flussi in {{site.data.keyword.appconserviceshort}} per connettere le tue applicazioni in modo che un evento che si verifichi in un'applicazione ne faccia verificare un altro in un'altra applicazione.  Puoi creare flussi guidati da eventi e flussi per le API   

Puoi utilizzare il dashboard {{site.data.keyword.appconserviceshort}} per monitorare i tuoi flussi e i tuoi server di integrazione per vedere quanto lavoro stanno svolgendo per tuo conto. Avviali e arrestali e modificali quando ne hai bisogno.

Qui spieghiamo le funzioni e la terminologia di {{site.data.keyword.appconserviceshort}} in modo più dettagliato.

-   [Flussi](#flows)
-   [Applicazioni](#apps)
-   [Azioni](#actions)
-   [Associazione di dati](#transforms)
-   [File BAR e server di integrazione](#barfiles)

## Flussi
{: #flows}

Puoi creare due tipi di flusso in {{site.data.keyword.appconserviceshort}}: un flusso guidato da eventi e un flusso per un'API.

In un flusso guidato da eventi, identifichi un evento che si può verificare nella tua prima applicazione (l'applicazione di origine) e le azioni che possono essere eseguite in una o più applicazioni di destinazione. Il flusso collega l'evento alle azioni in modo che, ogni volta che l'evento si verifica nell'applicazione di origine, l'azione viene automaticamente attivata nelle applicazioni di destinazione. Ogni azione completata correttamente viene conteggiata nel calcolo della tua quota mensile. Quando crei un flusso, aggiungi le tue applicazioni e scegli le azioni. Associ quindi i dati che vuoi trasferire tra le tue applicazioni.

Ad esempio, potresti creare un flusso che, ogni volta che qualcuno si registra come un nuovo partecipante con Eventbrite (l'evento), {{site.data.keyword.appconserviceshort}} richiama automaticamente i dettagli del partecipante da Salesforce e crea una nuova attività in Asana (le azioni).

![Un flusso multinodo, con l'applicazione di origine e due applicazioni di destinazione](images/multi_node_flow2.jpg)

Per ulteriori informazioni, vedi [Creating an event-driven flow ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/creating-event-driven-flow/).

Un flusso per un'API contiene una richiesta, una o più azioni dell'applicazione di destinazione e una risposta. La richiesta utilizza un modello che definisci per richiedere la creazione, la sostituzione o il richiamo di oggetti di dati nelle tue applicazioni. Quando la richiesta viene inoltrata, ogni applicazione di destinazione esegue la propria azione.  Il flusso restituisce quindi una risposta che conferma che le azioni sono state eseguite correttamente o restituisce i dati che erano stati richiesti.

![Un flusso per un'API che crea un prodotto in Salesforce](images/APIFlow2.jpg)

Per ulteriori informazioni, vedi [Creating flows for an API ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/creating-flows-api/).

Oltre ad aggiungere applicazioni ai tuoi flussi, puoi anche aggiungere nodi dalla scheda **Logic** per configurare il modo in cui elabori i dati. Ad esempio, utilizza il nodo If per aggiungere dell'elaborazione condizionale, ossia l'esecuzione di azioni differenti in base ai dati che ricevi (vedi [Adding conditional logic to a flow ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/adding-conditional-logic-flow/)). Utilizza invece il nodo **For each** quando vuoi eseguire un'azione per ogni record restituito da un'azione di richiamo (vedi [Retrieving items from your applications ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/using-ibm-app-connect-retrieve-items-applications/)).

Se sei uno sviluppatore di IBM Integration Bus o App Connect Enterprise, puoi anche creare delle soluzioni di integrazione complesse sviluppando dei flussi di messaggi nell'Integration Toolkit e assemblandoli in file BAR.

I tuoi flussi e i tuoi server di integrazione sono rappresentati da tile nel dashboard App Connect. I tile mostrano delle informazioni di riepilogo relative al flusso, all'API o al server di integrazione, ad esempio indicano se un flusso è in esecuzione o arrestato e se ha prodotto un errore. Puoi fare clic sulle icone di segno di spunta e di punto esclamativo per visualizzare quando il flusso è stato eseguito l'ultima volta con esito positivo o quali errori sono stati generati. Fai clic sui tre puntini ![L'icona di tre puntini verticali apre un menu per avviare, arrestare, modificare o eliminare il flusso](images/Menu.jpg) per aprire un menu per avviare, arrestare, modificare o eliminare le tue risorse. I flussi devono essere arrestati prima che sia possibile modificarli.

![Acquisizione di schermo che mostra i file dal dashboard per i flussi guidati da eventi, i flussi per le API e i server di integrazione](images/Dashboard.jpg)

## Applicazioni
{: #apps}

Quando creai dei flussi guidati da eventi o flussi per le API, le _applicazioni_ sono le applicazioni software basate sul cloud che stai connettendo. Puoi visualizzare un elenco delle applicazioni che puoi connettere a {{site.data.keyword.appconserviceshort}} nella pagina **Applications**. Fai clic su un'applicazione per acquisire ulteriori informazioni su di essa, per vedere quali eventi e azioni sono supportati e per stabilire una connessione al tuo account. Puoi connettere più account a ciascuna applicazione e passare dall'uno all'altro nella pagina Applications. Dopo che hai stabilito una connessione al tuo account, puoi anche aggiornare o rimuovere il tuo account nella pagina Applications.

![Acquisizione di schermo di una delle applicazioni nella pagina Applications](images/Magento2.jpg)

Non devi necessariamente stabilire una connessione alle tue applicazioni nella pagina Applications; puoi anche stabilire la connessione nell'editor di flussi mentre aggiungi le applicazioni al tuo flusso. Molte applicazioni richiedono solo un nome utente e una password ma altre richiedono più informazioni. Puoi determinare il modo in cui trovare queste informazioni nelle guide procedurali per le applicazioni ([How-to guides for apps ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://developer.ibm.com/integration/docs/app-connect/how-to-guides-for-apps/)).

Se stai utilizzando {{site.data.keyword.appconservicefull}} per eseguire soluzioni Integration Bus o App Connect Enterprise nel cloud, un'_applicazione_ è il contenitore in cui si trovano i flussi di messaggi, le librerie a altre risorse di cui ha bisogno la tua soluzione. 

## Azioni
{: #actions}

Puoi aggiungere diversi tipi di azione ai tuoi flussi. Le azioni comuni sono create (crea), retrieve (richiama) e update or create (aggiorna o crea), ma alcune applicazioni hanno delle azioni specifiche. Ad esempio, l'applicazione Watson Personality Insights ha un'azione denominata "Analyze personality". Puoi visualizzare un elenco delle azioni supportate per le applicazioni in {{site.data.keyword.appconserviceshort}} digitando il tipo di azione nel campo di ricerca nella pagina Applications.

![Acquisizione di schermo che mostra le azioni di richiamo supportate per le applicazioni](images/RetrieveApps2.jpg)

**create**

Come suggerito dal nome, l'azione create crea un oggetto o un record in un'applicazione. Ad esempio, se qualcuno si registra al tuo evento o inoltra un modulo completato, potresti voler creare un record per tale persona nell'applicazione CRM o di marketing. Oppure, se qualcuno apre un ticket nella tua applicazione help desk, potresti voler creare una email o un messaggio istantaneo per assicurarti che qualcuno se ne occupi immediatamente. Se c'è una possibilità che l'oggetto che vuoi creare possa esistere, puoi utilizzare invece un'azione *update or create*.

Per alcune applicazioni, potresti dover fornire delle informazioni supplementari quando aggiungi un'azione create a un flusso in modo che il tuo flusso sappia dove creare l'oggetto. Ad esempio, se stai utilizzando un'applicazione di gestione dei progetti come Asana o Trello, quando crei un'attività o una scheda devi specificare il progetto o la lavagna dove vuoi eseguirne l'aggiunta.

**update or create**

L'azione update or create modifica un record esistente nella tua applicazione di destinazione, se esiste, e crea invece il record, se non esiste. È nota anche come azione upsert (update or insert).

Ad esempio, poniamo che qualcuno inoltri un modulo Wufoo con una variazione dell'indirizzo. Se il contatto già è nel tuo sistema CRM, vuoi aggiornarne l'indirizzo ma, se non è invece presente, vuoi aggiungerlo. Analogamente all'azione di richiamo, quando scegli un'azione per aggiornare i dati in una delle tue applicazioni, puoi aggiungere una o più condizioni per assicurarti che stai aggiornando le informazioni corrette.

Se c'è più di un record nel tuo sistema di destinazione che corrisponde ai tuoi criteri, vedi un errore per il flusso nel dashboard e il flusso non aggiorna o crea alcun record. Ad esempio, è possibile che tu abbia più di un contatto con nome e cognome uguali. Puoi quindi provare a eseguire la messa in corrispondenza con un singolo contatto utilizzando dei dati univoci, come ad esempio il suo indirizzo email.

Probabilmente vedrai i seguenti codici di stato in risposta a un'azione di aggiornamento o creazione.
-   200 A record was updated
-   201 A record was created

Puoi utilizzare questi codici risposta in un secondo momento nel tuo flusso. Forse vuoi eseguire delle azioni differenti che dipendono del fatto che un record sia stato aggiornato o creato. Per un esempio di definizione di azioni basate sui codici di risposta, vedi l'esercitazione [Creating an event-driven flow that updates or creates a contact in Salesforce and updates Asana whenever you receive a form in Wufoo ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/creating-event-driven-flow-updates-creates-contact-salesforce-updates-asana-whenever-receive-form-wufoo/).

**retrieve**

L'azione di richiamo ottiene informazioni da un'applicazione in modo che tu possa utilizzarle in un'altra applicazione.

Quando aggiungi un'azione al tuo flusso per richiamare degli oggetti, puoi definire una o più condizioni per assicurarti che stai richiamando gli elementi corretti. Oppure, se vuoi richiamare tutti gli elementi di uno specifico tipo, puoi eliminare la condizione. Puoi anche definire quanti elementi vuoi richiamare e cosa succede se {{site.data.keyword.appconserviceshort}} ne trova di più o di meno del numero da te indicato.

Puoi gestire i tuoi elementi richiamati in due modi:
-   Puoi aggiungere un nodo "For each" dopo l'azione di richiamo per eseguire un'azione per ciascuno degli elementi che sono stati richiamati.
-   Puoi aggiungere un'altra azione dopo l'azione di richiamo per elaborare l'elenco di elementi richiamati. Questa è un'azione singola, indipendentemente da quanti elementi vengano restituiti – come ad esempio la creazione di una email che elenca tutti gli elementi richiamati.

Puoi anche decidere quale azione eseguire in base al codice di stato che ottieni in risposta all'azione di richiamo. Puoi utilizzare un nodo “If” per eseguire azioni differenti per i differenti codici di stato. Probabilmente vedrai i seguenti codici di stato in risposta a un'azione di richiamo.
-   204 No records were found
-   200 All records in the application match the condition
-   206 The specified maximum number of records were retrieved, but more matching records exist in the application

Per ulteriori informazioni, vedi [Retrieving items from your applications ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/using-ibm-app-connect-retrieve-items-applications/).

## Associazione di dati
{: #transforms}

Dopo che hai creato un flusso, aggiunto le tue applicazioni e selezionato le azioni appropriate, devi specificare quali informazioni vuoi trasferire tra le tue applicazioni. Puoi vedere nell'editor di flusso che, quando aggiungi un'azione al tuo flusso, vedi un elenco di campi disponibili per tale applicazione. Puoi popolare questi campi con i dati dalla tua applicazione di origine o dalle azioni precedenti nel flusso.

Alcuni campi sono obbligatori e sono contrassegnati con un asterisco. Ad esempio, quando stai creando un lead in Salesforce, devi specificare un cognome:

![Acquisizione di schermo che mostra che il campo Last name è obbligatorio](images/LastName.jpg)

Quando fai clic in uno si questi campi, vedi un paio di icone: **Insert reference** ![Icona Insert reference](images/InsertRef.jpg) and **Apply a Function** ![Icona Apply a function](images/Functions.jpg). Se fai clic su **Insert reference**, vedi i dati disponibili che puoi inserire in tale campo dalle applicazioni precedenti nel flusso. Il seguente esempio mostra che possiamo scegliere i campi dall'applicazione di origine Wufoo o da un'azione Salesforce precedente nel flusso. Puoi anche utilizzare il codice di stato dall'azione update or create di Salesforce.

![Acquisizione di schermo che mostra gli input disponibili per un'associazione di dati](images/Inputs.jpg)

Nel seguente esempio, il nostro flusso viene attivato quando un nuovo modulo completato viene ricevuto in Wufoo. Vogliamo creare un contatto a Salesforce per la persona che ha inoltrato il modulo. Quindi, quando aggiungiamo la nostra azione "Create contact" di Salesforce al flusso, copiamo i dettagli per il nostro contatto dal modulo Wufoo. Qui possiamo vedere che, per il cognome del contatto Salesforce, selezioniamo il cognome dell'utente che ha inoltrato il modulo Wufoo. Puoi vedere che il campo associato proviene da Wufoo grazie al colore:

![Acquisizione di schermo che mostra che il campo Last name di Wufoo è associato al campo Last name di Salesforce](images/Mapping.jpg)

Nel seguente esempio, aggiungiamo un'azione "Create message" di Slack al flusso dopo un'azione "Update or create contact" di Salesforce. Vogliamo inserire un messaggio in Slack per indicare quale codice di risposta viene ricevuto per l'azione di Salesforce:

![Acquisizione di schermo di un'azione Create message di Slack che corrisponde a un codice di risposta](images/SlackSC.jpg)

Puoi vedere che, nel campo **Text** per l'azione "Create message" di Slack, digitiamo un messaggio ed associamo quindi il codice di stato per l'azione "Update or create contact" di Salesforce.

Ecco un altro esempio di associazione dei codici di risposta in un modo differente. Questa volta, aggiungiamo un nodo "If" dopo un'azione "Update or create contact" di Salesforce perché vogliamo eseguire delle azioni differenti a seconda del fatto che venga aggiornato un contatto Salesforce esistente oppure venga creato un nuovo contatto. In questo caso, un codice di risposta "200" significa che il contatto viene aggiornato. Pertanto, questo ramo del nodo "If" contiene un'azione specifica per un record aggiornato.

![Acquisizione di schermo che mostra in che modo vengono utilizzati i codici di risposta in un nodo If](images/IfSC.jpg)

L'icona **Apply a function** ![Icona Apply a function](images/Functions.jpg) ti mostra un elenco delle funzioni di trasformazione che puoi usare per personalizzare i dati che stai passando attraverso il tuo flusso. Queste funzioni possono essere tanto semplici quanto la conversione di uno specifico campo in testo in maiuscolo o minuscolo oppure leggermente più complesse, come ad esempio la ricerca e la sostituzione di specifici modelli nei dati. Possono anche essere potenti al punto da formare delle espressioni regolari. Puoi selezionare la funzione che desideri dall'elenco oppure puoi digitarla tu stesso. La sintassi delle funzioni è JSONata, un linguaggio di query e trasformazione semplice. Per ulteriori informazioni, vedi [http://jsonata.org ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](http://jsonata.org).


## File BAR e server di integrazione
{: #barfiles}

Un file BAR è un file compresso a cui aggiungi risorse distribuibili in IBM Integration Bus o App Connect Enterprise.  Quando sviluppi una soluzione di integrazione in Integration Bus o App Connect Enterprise, assembli i tuoi flussi di messaggi e tutte le risorse utilizzate da tali flussi di messaggi in un file BAR. Distribuisci quindi il file BAR ad un server di integrazione.  Tale server può essere in loco o in {{site.data.keyword.appconserviceshort}}.  Puoi eseguire le tue soluzioni Integration Bus o App Connect Enterprise in App Connect, senza dover acquisire e mantenere un'infrastruttura IT.  Quando carichi un file BAR su App Connect, viene creato un server di integrazione per eseguire il contenuto del file BAR.  Puoi configurare l'autenticazione di base e la connettività protetta tra le tue risorse basate sul cloud e in loco (vedi [Running your Integration Bus solutions in App Connect ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan)).  
