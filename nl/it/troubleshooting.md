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


# Risoluzione dei problemi di IBM App Connect
{: #troubleshooting}

Per risolvere i problemi con i flussi e i server di integrazione {{site.data.keyword.appconservicefull}}, puoi visualizzare i log in Kibana. Se hai domande o problemi quando usi {{site.data.keyword.appconserviceshort}}, ottieni assistenza cercando informazioni o facendo domande tramite un forum. Quando usi i forum per fare una domanda, contrassegna con delle tag la tua domanda in modo che sia vista dai team di sviluppo di {{site.data.keyword.Bluemix}} e {{site.data.keyword.appconserviceshort}}.

-   Guarda il tile per un flusso in esecuzione nel dashboard {{site.data.keyword.appconserviceshort}}. Se c'è un segno di spunta verde, il flusso è in esecuzione correttamente; fai clic sul segno di spunta per vedere quando è stato attivato l'ultima volta il flusso.

    ![Acquisizione di schermo che mostra che un flusso è in esecuzione correttamente](/images/SuccessfulFlow.jpg)

    Se c'è un punto esclamativo rosso, c'è un problema; fai clic sul punto esclamativo per scoprire qual è il problema. ![Acquisizione di schermo che mostra che un flusso ha un problema](/images/ErroredFlow.jpg)

-   Controlla la pagina dello stato di {{site.data.keyword.appconserviceshort}} per vedere se vengono notificati eventuali problemi o se è pianificata qualche attività di manutenzione: [Pagina dello stato di {{site.data.keyword.appconserviceshort}} ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://developer.ibm.com/integration/docs/app-connect/app-connect-status/)
-   Per visualizzare le informazioni di log per i tuoi flussi, fai clic su **Logs** nel menu {{site.data.keyword.appconserviceshort}}. I messaggi di errore e informativi per i tuoi flussi sono visualizzati per impostazione predefinita in Kibana, dove puoi visualizzare i dati per uno specifico intervallo temporale oppure utilizzare i filtri per visualizzare specifici tipi di informazioni. Per visualizzare le informazioni di debug per i tuoi flussi, apri il menu su un tile di flusso nel dashboard {{site.data.keyword.appconserviceshort}} e seleziona quindi **Enable debug logging**.  Devi quindi riavviare il tuo flusso perché venga avviata la registrazione in log del debug. Quando abiliti la registrazione in log del debug, le voci di log di debug, che potenzialmente includono dati di payload, sono visibili agli operatori IBM. Per saperne di più sulla registrazione in log del debug, vedi [Debugging your message flows in {{site.data.keyword.appconserviceshort}} ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/debugging-message-flows-ibm-app-connect/).  Per ulteriori informazioni su Kibana, vedi la [documentazione di Kibana ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://www.elastic.co/guide/en/kibana/4.0/discover.html).
-   Per visualizzare le informazioni di log per i tuoi server di integrazione, apri un server di integrazione e fai clic su **Download logs** o **View logs**.  Per visualizzare i log per un server di integrazione in Kibana, devi collegare una politica di registrazione in log a tale server di integrazione (vedi [Viewing logs for your integration servers ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/viewing-logs-for-your-integration-servers-in-app-connect-enterprise-beta)).
-   Trova le risposte alle domande comuni su {{site.data.keyword.appconserviceshort}} in [Frequently asked questions about {{site.data.keyword.appconserviceshort}} ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://developer.ibm.com/integration/docs/app-connect/faq/).
-   Attieniti alle istruzioni dettagliate su come connettere le tue applicazioni in [Tutorials for {{site.data.keyword.appconserviceshort}} ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/).
-   Per domande sul servizio e istruzioni introduttive, utilizza il forum [IBM dW Answers ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://developer.ibm.com/answers/topics/app_connect). Includi le tag "ibm_cloud" e "app_connect" (con un carattere di sottolineatura).

    Per ulteriori informazioni sull'utilizzo dei meccanismi di supporto di {{site.data.keyword.Bluemix}}, vedi [Supporto ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://cloud.ibm.com/unifiedsupport/supportcenter).

## Notifica di un problema al team IBM App Connect
{: #reporting}

Se hai seguito il suggerimento per la risoluzione del problema e continui a riscontrarlo, puoi ottenere assistenza dal team {{site.data.keyword.appconserviceshort}}.  Dal menu {{site.data.keyword.appconserviceshort}}, fai clic su **Contatti** e quindi su **Come ottenere supporto**.  Esegui l'accesso con il tuo ID IBM, fai clic su **Create a case** e fornisci quante più puoi delle seguenti informazioni, (Puoi anche fare clic su **Supporto** nella console {{site.data.keyword.Bluemix}}). 

* La regione {{site.data.keyword.Bluemix}} dove viene eseguito il provisioning della tua istanza di {{site.data.keyword.appconserviceshort}}. (Ad esempio, Dallas o Londra).
* L'ID istanza del servizio {{site.data.keyword.appconserviceshort}} che stai utilizzando. (Puoi trovare questo ID consultando le informazioni sull'account in {{site.data.keyword.appconserviceshort}} Instance Identifier).
* Il problema che stai sperimentando. (Ad esempio, se il problema è con un'applicazione o una funzione specifiche).
* L'ID batch, se il problema è correlato all'elaborazione batch. Se si verificano degli errori in un processo batch, e hai definito un ID per ciascun record nel processo batch, puoi trovare il tuo ID definito nella colonna "batch-record-id_str" del log Kibana; vedi [How to use batch processing in {{site.data.keyword.appconserviceshort}} ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://developer.ibm.com/integration/docs/app-connect/toolbox-utilities/how-to-use-batch-processing-in-ibm-app-connect/).)
* La data e l'ora (compreso il fuso orario) quando si è verificato il problema per la prima volta e il periodo di tempo per cui il flusso era stato in esecuzione prima che si verificasse il problema.
* Se il problema continua a verificarsi e se puoi replicarlo.
* Se applicabile, il tipo e la versione del browser che stai utilizzando. (Supportiamo solo le ultime versioni del browser).
* Qualsiasi voce di log che descrive il problema.
* L'impatto che il problema sta avendo sulla tua attività di business.
