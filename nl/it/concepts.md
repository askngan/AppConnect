---

copyright:
  years: 2017
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

Ci sono due tipi di risorsa che puoi eseguire in {{site.data.keyword.appconserviceshort}} per connettere le tue applicazioni, a seconda delle tue esigenze di business: server di integrazione e flussi.  Per eseguire le tue soluzioni IBM Integration Bus o App Connect Enterprise in {{site.data.keyword.appconserviceshort}}, carichi una soluzione di integrazione in un file BAR e lo esegui quindi in un server di integrazione in {{site.data.keyword.appconserviceshort}}.  Crei i flussi in {{site.data.keyword.appconserviceshort}} per connettere le tue applicazioni in modo che un evento che si verifichi in un'applicazione ne faccia verificare un altro in un'altra applicazione.  Puoi creare flussi guidati dagli eventi e flussi per le API.

Puoi utilizzare il dashboard {{site.data.keyword.appconserviceshort}} per monitorare i tuoi flussi e i tuoi server di integrazione per vedere quanto lavoro stanno svolgendo per tuo conto. Avviali e arrestali e modificali quando ne hai bisogno.

Qui spiegheremo le funzioni e la terminologia di {{site.data.keyword.appconserviceshort}}:

-   [Flussi](#flows)
-   [Applicazioni](#apps)
-   [Azioni](#actions)
-   [Associazione di dati](#transforms)
-   [File BAR e server di integrazione](#barfiles)

## Flussi
{: #flows}

Ci sono due tipi di flusso che puoi creare in {{site.data.keyword.appconserviceshort}}: un flusso guidato dagli eventi e un flusso per un'API.

In un flusso guidato dagli eventi, identifichi un evento che si può verificare nella tua prima applicazione (l'applicazione di origine) e le azioni che possono essere eseguite in una o più applicazioni di destinazione. Il flusso collega l'evento alle azioni in modo che, ogni volta che l'evento si verifica nell'applicazione di origine, l'azione viene automaticamente attivata nelle applicazioni di destinazione. Ogni azione completata correttamente viene conteggiata nel calcolo della tua quota mensile. Quando crei un flusso, aggiungi le tue applicazioni e scegli le azioni. Associ quindi i dati che vuoi trasferire tra le tue applicazioni.

Ad esempio, potresti creare un flusso che, ogni volta che qualcuno si registra come un nuovo partecipante con Eventbrite (l'evento), {{site.data.keyword.appconserviceshort}} richiama automaticamente i dettagli del partecipante da Salesforce e crea una nuova attività in Asana (le azioni).

![Un flusso multinodo, con l'applicazione di origine e due applicazioni di destinazione](images/multi_node_flow2.jpg)

Per ulteriori informazioni, vedi [Creating an event-driven flow ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/creating-event-driven-flow/).

Un flusso per un'API contiene una richiesta, una o più azioni dell'applicazione di destinazione e una risposta. La richiesta utilizza un modello che definisci per richiedere la creazione, la sostituzione o il richiamo di oggetti di dati nelle tue applicazioni. Quando la richiesta viene inoltrata, ogni applicazione di destinazione esegue la propria azione e il flusso restituisce quindi una risposta che conferma che le azioni sono state eseguite correttamente o che restituisce i dati che erano stati richiesti.

![Un flusso per un'API che crea un prodotto in Salesforce](images/APIFlow2.jpg)

Per ulteriori informazioni, vedi [Creating flows for an API ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/creating-flows-api/).

Oltre ad aggiungere applicazioni ai tuoi flussi, puoi anche aggiungere nodi dalla scheda **Logic** che ti consentono di configurare il modo in cui elabori i dati. Ad esempio, utilizza il nodo If per aggiungere dell'elaborazione condizionale, ossia l'esecuzione di azioni differenti in base ai dati che ricevi (vedi [Adding conditional logic to a flow ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/adding-conditional-logic-flow/)). Utilizza invece il nodo For each quando vuoi eseguire un'azione per ogni record restituito da un'azione retrieve (vedi [Retrieving items from your applications ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/using-ibm-app-connect-retrieve-items-applications/)).

Se sei uno sviluppatore di IBM Integration Bus o App Connect Enterprise, puoi anche creare delle soluzioni di integrazione complesse sviluppando dei flussi di messaggi nell'Integration Toolkit e assemblandoli in file BAR.

I tuoi flussi e i tuoi server di integrazione sono rappresentati da tile nel dashboard App Connect. I tile mostrano delle informazioni di riepilogo relative al flusso, all'API o al server di integrazione, ad esempio indicano se un flusso è in esecuzione o arrestato e se la sua esecuzione è stata eseguita correttamente o se ha prodotto un errore. Puoi fare clic sulle icone di segno di spunta e di punto esclamativo per visualizzare quando il flusso è stato eseguito l'ultima volta con esito positivo o quali errori sono stati generati. Fai clic sui tre puntini ![L'icona di tre puntini verticali apre un menu per avviare, arrestare, modificare o eliminare il flusso](images/Menu.jpg) per aprire un menu che ti consente di avviare, arrestare, modificare o eliminare le tue risorse. I flussi devono essere arrestati prima che sia possibile modificarli.

![Acquisizione di schermo che mostra i tile dal dashboard per i flussi guidati da eventi, i flussi per le API e i server di integrazione](images/Dashboard.jpg)

## Applicazioni
{: #apps}

Quando crei dei flussi guidati da eventi o flussi per le API, le _applicazioni_ sono le applicazioni software basate sul cloud che stai connettendo. Puoi visualizzare un elenco delle applicazioni che puoi connettere a {{site.data.keyword.appconserviceshort}} nella pagina **Applications**. Fai clic su un'applicazione per acquisire ulteriori informazioni su di essa, per vedere quali eventi e azioni sono supportati e per stabilire una connessione al tuo account. Puoi avere più account connessi a ciascuna applicazione e passare dall'uno all'altro nella pagina Applications. Dopo che hai stabilito una connessione al tuo account, puoi anche aggiornare o rimuovere il tuo account in tale pagina.

![Acquisizione di schermo delle applicazioni nella pagina Applications](images/Magento2.jpg)

Non devi necessariamente stabilire una connessione alle tue applicazioni nella pagina Applications; puoi anche stabilire la connessione nell'editor di flussi mentre aggiungi le applicazioni al tuo flusso. Molte applicazioni richiedono solo un nome utente e una password ma altre richiedono più informazioni. Puoi determinare il modo in cui trovare queste informazioni nelle guide procedurali per le applicazioni ([How-to guides for apps ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://developer.ibm.com/integration/docs/app-connect/how-to-guides-for-apps/)).

Se stai utilizzando {{site.data.keyword.appconservicefull}} per eseguire soluzioni Integration Bus o App Connect Enterprise nel cloud, un'_applicazione_ è il contenitore in cui si trovano i flussi di messaggi, le librerie a altre risorse di cui ha bisogno la tua soluzione. 

## Azioni
{: #actions}

Puoi aggiungere diversi tipi di azione ai tuoi flussi. Le azioni comuni sono create (crea), retrieve (richiama) e update or create (aggiorna o crea), ma alcune applicazioni hanno delle azioni specifiche. Ad esempio, le applicazioni Equals 3 Lucy hanno un'azione denominata "Ask Lucy" e l'applicazione Watson Personality Insights ha un'azione denominata "Analyze personality". Puoi visualizzare un elenco delle azioni supportate per le applicazioni in {{site.data.keyword.appconserviceshort}} digitando il tipo di azione nel campo di ricerca nella parte superiore della pagina Applications:

![Acquisizione di schermo che mostra le azioni retrieve supportate per le applicazioni](images/RetrieveApps2.jpg)

**create**

Come suggerito dal nome, l'azione create crea un oggetto o un record in un'applicazione. Ad esempio, se qualcuno si registra al tuo evento o inoltra un modulo completato, potresti voler creare un record per tale persona nell'applicazione CRM o di marketing. Oppure, se qualcuno apre un ticket nella tua applicazione help desk, potresti voler creare una email o un messaggio istantaneo per assicurarti che qualcuno se ne occupi immediatamente. Se c'è una possibilità che l'oggetto che vuoi creare possa già esistere, puoi utilizzare invece un'azione *update or create*.

Per alcune applicazioni, potresti dover fornire delle informazioni supplementari quando aggiungi un'azione create a un flusso in modo che il tuo flusso sappia dove creare l'oggetto. Ad esempio, se stai utilizzando un'applicazione di gestione dei progetti come Asana o Trello, quando crei un'attività o una scheda dovrai specificare il progetto o la lavagna dove vuoi eseguirne l'aggiunta.

**update or create**

L'azione update or create modifica un record esistente nella tua applicazione di destinazione, se esiste, e crea invece il record, se non esiste già. È nota anche come azione upsert (update or insert).

Ad esempio, poniamo che qualcuno abbia inoltrato un modulo Wufoo con una variazione dell'indirizzo. Se il contatto già è nel tuo sistema CRM, vuoi aggiornarne l'indirizzo ma, se non è invece presente, vuoi aggiungerlo. Analogamente all'azione retrieve, quando scegli un'azione per aggiornare i dati in una delle tue applicazioni, puoi aggiungere una o più condizioni per assicurarti che stai aggiornando le informazioni corrette.

Se c'è più di un record nel tuo sistema di destinazione che corrisponde ai tuoi criteri, vedrai un errore per il flusso nel dashboard e il flusso non aggiornerà o creerà alcun record. Ad esempio, è possibile che tu abbia più di un contatto con nome e cognome uguali. Puoi quindi provare a eseguire la messa in corrispondenza con un singolo contatto utilizzando dei dati univoci, come ad esempio il suo indirizzo email.

I codici di stato che probabilmente vedrai nella risposta a un'azione update or create sono:

-   200: A record was updated
-   201: A record was created

Puoi utilizzare questi codici risposta in un secondo momento nel tuo flusso. Forse vuoi eseguire delle azioni differenti a seconda del fatto che un record sia stato aggiornato o creato. Per un esempio di definizione di azioni basate sui codici di risposta, vedi l'esercitazione [Creating an event-driven flow that updates or creates a contact in Salesforce and updates Asana whenever you receive a form in Wufoo](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/creating-event-driven-flow-updates-creates-contact-salesforce-updates-asana-whenever-receive-form-wufoo/).

**retrieve**

L'azione retrieve ottiene informazioni da un'applicazione in modo che tu possa utilizzarle in un'altra applicazione.

Quando aggiungi un'azione al tuo flusso per richiamare degli oggetti, puoi definire una o più condizioni per assicurarti che stai richiamando gli elementi corretti. Oppure, se vuoi solo richiamare tutti gli elementi di uno specifico tipo, puoi eliminare la condizione. Puoi anche definire quanti elementi vuoi richiamare e cosa succede se {{site.data.keyword.appconserviceshort}} ne trova di più o di meno del numero da te indicato.

Puoi gestire i tuoi elementi richiamati in due modi:

-   Puoi aggiungere un nodo "For each" dopo l'azione retrieve per eseguire un'azione per ciascuno degli elementi che sono stati richiamati.
-   Puoi aggiungere un'altra azione dopo l'azione retrieve per elaborare l'elenco di elementi richiamati. Questa è un'azione singola, indipendentemente da quanti elementi vengano restituiti – come ad esempio la creazione di una email che elenca tutti gli elementi richiamati.

Puoi anche decidere quale azione eseguire in base al codice di stato che ottieni in risposta all'azione retrieve. Puoi utilizzare un nodo “If” per eseguire azioni differenti per i differenti codici di stato. I codici di stato che probabilmente vedrai nella risposta a un'azione retrieve sono:

-   204: No records were found
-   200: All records in the application match the condition
-   206: The specified maximum number of records were retrieved, but more matching records exist in the application

Per ulteriori informazioni, vedi [Retrieving items from your applications](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/using-ibm-app-connect-retrieve-items-applications/).

## Associazione di dati
{: #transforms}

Dopo che hai creato un flusso, aggiunto le tue applicazioni e selezionato le azioni appropriate, devi specificare quali informazioni vuoi trasferire tra le tue applicazioni. Vedrai nell'editor di flusso che, quando aggiungi un'azione al tuo flusso, verrà visualizzato un elenco dei campi disponibili per tale applicazione, che puoi compilare con i dati dalla tua applicazione di origine o dalle azioni precedenti nel flusso.

Alcuni campi sono obbligatori e sono contrassegnati con un asterisco. Ad esempio, quando stai creando un lead in Salesforce, devi specificare un cognome:

![Acquisizione di schermo che mostra che il campo Last name è obbligatorio](images/LastName.jpg)

Quando fai clic in uno si questi campi, vedrai un paio di icone: **Insert reference**![Icona Insert reference](images/InsertRef.jpg) and **Apply a Function**![Icona Apply a function](images/Functions.jpg). Se fai clic su **Insert reference**, vedrai i dati disponibili che puoi inserire in tale campo dalle applicazioni precedenti nel flusso. Il seguente esempio mostra che possiamo scegliere i campi dall'applicazione di origine Wufoo o da un'azione Salesforce precedente nel flusso. Puoi anche utilizzare il codice di stato dall'azione update or create di Salesforce.

![Acquisizione di schermo che mostra gli input disponibili per un'associazione di dati](images/Inputs.jpg)

Nel seguente esempio, il nostro flusso viene attivato da un nuovo modulo completato che viene ricevuto in Wufoo. Vogliamo creare un contatto in Salesforce per la persona che ha inoltrato il modulo. Quindi, quando aggiungiamo la nostra azione "Create contact" di Salesforce al flusso, copiamo i dettagli per il nostro contatto dal modulo Wufoo. Qui possiamo vedere che, per il cognome del contatto Salesforce, abbiamo selezionato il cognome dell'utente che ha inoltrato il modulo Wufoo. Puoi vedere che il campo associato proviene da Wufoo grazie al colore:

![Acquisizione di schermo che mostra che il campo Last name di Wufoo è associato al campo Last name di Salesforce](images/Mapping.jpg)

Nel seguente esempio, abbiamo aggiunto un'azione "Create message" di Slack al flusso dopo un'azione "Update or create contact" di Salesforce. Vogliamo semplicemente mettere un messaggio su Slack per indicare quale codice di risposta è stato ricevuto per l'azione di Salesforce:

![Acquisizione di schermo di un'azione Create message di Slack che corrisponde a un codice di risposta](images/SlackSC.jpg)

Puoi vedere che, nel campo **Text** per l'azione "Create message" di Slack, abbiamo digitato un messaggio ed associato quindi il codice di stato per l'azione "Update or create contact" di Salesforce.

Ecco un altro esempio di associazione dei codici di risposta in un modo differente. Questa volta, abbiamo aggiunto un nodo "If" dopo un'azione "Update or create contact" di Salesforce perché vogliamo eseguire delle azioni differenti a seconda del fatto che sia stato aggiornato un contatto Salesforce esistente oppure sia stato creato un nuovo contatto. In questo caso, un codice di risposta "200" significa che il contatto è stato aggiornato. Pertanto, questo ramo del nodo "If" conterrà un'azione specifica per un record aggiornato.

![Acquisizione di schermo che mostra i codici di risposta utilizzati in un nodo If](images/IfSC.jpg)

L'icona **Apply a function** ![Icona Apply a function](Functions.jpg) ti mostra un elenco delle funzioni di trasformazione che puoi usare per personalizzare i dati che stai passando attraverso il tuo flusso. Queste funzioni possono essere tanto semplici quanto la conversione di uno specifico campo in maiuscole o minuscole oppure leggermente più complesse, come ad esempio la ricerca e la sostituzione di specifici modelli nei dati. Possono anche essere potenti al punto da formare delle espressioni regolari. Puoi selezionare la funzione che desideri dall'elenco oppure puoi digitarla tu stesso. La sintassi delle funzioni è JSONata, un linguaggio di query e trasformazione semplice. Per ulteriori informazioni, consulta [http://jsonata.org](http://jsonata.org).


## File BAR e server di integrazione
{: #barfiles}

Un file BAR è un file compresso a cui aggiungi risorse distribuibili in IBM Integration Bus o App Connect Enterprise.  Quando sviluppi una soluzione di integrazione in Integration Bus o App Connect Enterprise, assembli i tuoi flussi di messaggi e tutte le risorse utilizzate da tali flussi di messaggi in un file BAR e distribuisci quindi il file BAR a un server di integrazione. Tale server può essere in loco o in {{site.data.keyword.appconserviceshort}}.  Puoi eseguire le tue soluzioni Integration Bus o App Connect Enterprise in App Connect, senza dover acquisire e mantenere un'infrastruttura IT. Quando carichi un file BAR su App Connect, viene creato un server di integrazione per eseguire il contenuto del file BAR. Puoi configurare l'autenticazione di base e la connettività protetta tra le tue risorse basate sul cloud e in loco (vedi [Running your Integration Bus solutions in App Connect ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan)).  
