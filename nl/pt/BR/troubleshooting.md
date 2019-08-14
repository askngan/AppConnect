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


# Solucionando problemas do IBM App Connect
{: #troubleshooting}

Para solucionar problemas com fluxos e servidores de integração do {{site.data.keyword.appconservicefull}}, é possível visualizar logs no Kibana. Se você tiver perguntas ou problemas quando estiver usando o {{site.data.keyword.appconserviceshort}}, obtenha ajuda procurando informações ou fazendo perguntas por meio de um fórum. Ao usar os fóruns para fazer uma pergunta, identifique sua pergunta para que ela seja vista pelas equipes de desenvolvimento do {{site.data.keyword.Bluemix}} e do {{site.data.keyword.appconserviceshort}}.

-   Consulte o bloco para um fluxo em execução no painel do {{site.data.keyword.appconserviceshort}}. Se houver uma marcação verde, o fluxo está executando com êxito. Clique na marcação para ver quando o fluxo foi acionado pela última vez.

    ![Captura de tela que mostra que um fluxo está executando com sucesso](/images/SuccessfulFlow.jpg)

    Se houver um ponto de exclamação vermelho, há um problema. Clique no ponto de exclamação para descobrir qual é o problema. ![Captura de tela que mostra que um fluxo tem um problema](/images/ErroredFlow.jpg)

-   Verifique a página de status do {{site.data.keyword.appconserviceshort}} para ver se algum problema é relatado ou a manutenção está planejada: [página de status do {{site.data.keyword.appconserviceshort}} ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://developer.ibm.com/integration/docs/app-connect/app-connect-status/)
-   Para visualizar informações de log para os seus fluxos, clique em **Logs** no menu do {{site.data.keyword.appconserviceshort}}. As mensagens de erro e de informações para os fluxos são mostradas por padrão no Kibana, em que é possível visualizar os dados para um intervalo de tempo específico ou use filtros para mostrar determinados tipos de informações. Para visualizar as informações sobre depuração para os fluxos, abra o menu em um bloco do fluxo no painel do {{site.data.keyword.appconserviceshort}} e, em seguida, selecione **Ativar a criação de log de depuração**.  Em seguida, é necessário reiniciar o fluxo para que a criação de log de depuração seja iniciada.  Quando você ativa a criação de log de depuração, as entradas de log de depuração, potencialmente incluindo dados de carga útil, são visíveis para os operadores da IBM. Para saber mais sobre a criação de log de depuração, consulte [Depurando seus fluxos de mensagens no {{site.data.keyword.appconserviceshort}}![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/debugging-message-flows-ibm-app-connect/).  Para saber mais sobre o Kibana, consulte a [Documentação do Kibana ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://www.elastic.co/guide/en/kibana/4.0/discover.html).
-   Para visualizar a informação de log para os servidores de integração, abra um servidor de integração e clique em **Fazer download de logs** ou **Visualizar logs**.  Para visualizar os logs de um servidor de integração no Kibana, deve-se anexar uma política de criação de log a esse servidor de integração (consulte [Visualizando logs para os seus servidores de integração![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/viewing-logs-for-your-integration-servers-in-app-connect-enterprise-beta)).
-   Localize respostas para perguntas comuns sobre o {{site.data.keyword.appconserviceshort}} em [Perguntas frequentes sobre o {{site.data.keyword.appconserviceshort}} ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://developer.ibm.com/integration/docs/app-connect/faq/).
-   Siga as instruções passo a passo sobre como conectar seus aplicativos nos [Tutoriais para o {{site.data.keyword.appconserviceshort}} ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/).
-   Para perguntas sobre o serviço e instruções de introdução, use o fórum [IBM dW Answers ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://developer.ibm.com/answers/topics/app_connect). Inclua as tags "ibm_cloud" e "app_connect" (com um sublinhado).

    Para obter mais informações sobre como usar os mecanismos de suporte do {{site.data.keyword.Bluemix}}, consulte [Suporte ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://cloud.ibm.com/unifiedsupport/supportcenter).

## Relatando um problema para a equipe do IBM App Connect
{: #reporting}

Se você seguiu o aviso de resolução de problemas e ainda está enfrentando um problema, poderá obter ajuda da equipe do {{site.data.keyword.appconserviceshort}}.  No menu do {{site.data.keyword.appconserviceshort}}, clique em **Entre em contato conosco** e, em seguida, **Obter suporte**.  Conecte-se com seu IBMid, clique em **Criar um caso** e forneça o máximo das informações a seguir conforme possível. (Também é possível clicar em **Suporte** no console do {{site.data.keyword.Bluemix}}.) 

* A região do {{site.data.keyword.Bluemix}} na qual sua instância do {{site.data.keyword.appconserviceshort}} é provisionada. (Por exemplo, Dallas ou Londres.)
* O ID da instância do serviço do {{site.data.keyword.appconserviceshort}} que você está usando. (É possível localizar esse ID verificando as informações da conta no {{site.data.keyword.appconserviceshort}} Instance Identifier.)
* O problema que você está experimentando. (Por exemplo, se o problema é com uma função ou aplicativo específico.)
* O ID do lote se o problema estiver relacionado ao processamento em lote. (Se ocorrerem erros em um processo em lote e você tiver definido um ID para cada registro no processo em lote, será possível localizar seu ID definido na coluna "batch-record-id_str" do log do Kibana. Consulte [Como usar o processamento em lote no {{site.data.keyword.appconserviceshort}} ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://developer.ibm.com/integration/docs/app-connect/toolbox-utilities/how-to-use-batch-processing-in-ibm-app-connect/).)
* A data e hora (incluindo o fuso horário) quando o problema ocorreu pela primeira vez e o período de tempo em que o fluxo estava em execução antes de o problema ter ocorrido.
* Se o problema ainda continuar ocorrendo e se você puder replicá-lo.
* Se aplicável, o tipo de navegador e a versão que você está usando. (Suportamos somente as versões mais recentes do navegador.)
* Qualquer entrada de log que descreve o problema.
* O impacto que o problema está tendo em seu negócio.
