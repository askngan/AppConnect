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


# Solucionando problemas do IBM App Connect
{: #troubleshooting}

Para solucionar problemas com fluxos e servidores de integração do {{site.data.keyword.appconservicefull}}, é possível visualizar logs no Kibana. Se você tiver perguntas ou problemas quando estiver usando o {{site.data.keyword.appconserviceshort}}, obtenha ajuda procurando informações ou fazendo perguntas por meio de um fórum. Ao usar os fóruns para fazer uma pergunta, identifique sua pergunta para que ela seja vista pelas equipes de desenvolvimento do {{site.data.keyword.Bluemix}} e do {{site.data.keyword.appconserviceshort}}.

-   Consulte o bloco para um fluxo em execução no painel do {{site.data.keyword.appconserviceshort}}. Se houver uma marcação verde, o fluxo foi executado com êxito. Clique na marcação para ver quando o fluxo foi acionado pela última vez.

    ![Captura de tela mostrando que um fluxo foi executado com êxito](/images/SuccessfulFlow.jpg)

    Se houver um ponto de exclamação vermelho, haverá um problema. Clique no ponto de exclamação para descobrir o que deu errado. ![Captura de tela mostrando que um fluxo tem um problema](/images/ErroredFlow.jpg)

-   Verifique a página de status do {{site.data.keyword.appconserviceshort}} para ver se há algum problema conhecido atual ou se qualquer manutenção está planejada: página de status do [{{site.data.keyword.appconserviceshort}} ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://developer.ibm.com/integration/docs/app-connect/app-connect-status/)
-   Para visualizar as informações de log para os fluxos, clique em **Logs** no menu hambúrguer do {{site.data.keyword.appconserviceshort}}. As mensagens de erro e de informações para os fluxos são mostradas por padrão no Kibana, em que é possível visualizar os dados para um intervalo de tempo específico ou use filtros para mostrar determinados tipos de informações. Para visualizar as informações sobre depuração para os fluxos, abra o menu em um bloco do fluxo no painel do {{site.data.keyword.appconserviceshort}} e, em seguida, selecione **Ativar a criação de log de depuração**.  Você, então, precisará reiniciar o fluxo para que a criação de log de depuração seja iniciada. Observe que ao ativar a criação de log de depuração, as entradas de log de depuração, potencialmente incluindo os dados de carga útil, são visíveis para os operadores da IBM. Para saber mais sobre a criação de log de depuração, consulte [Depurando fluxos de mensagens no {{site.data.keyword.appconserviceshort}}](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/debugging-message-flows-ibm-app-connect/). Para saber mais sobre o Kibana, consulte a [Documentação do Kibana ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://www.elastic.co/guide/en/kibana/4.0/discover.html).
-   Para visualizar a informação de log para os servidores de integração, abra um servidor de integração e clique em **Fazer download de logs** ou **Visualizar logs**. Para visualizar os logs de um servidor de integração no Kibana, é necessário anexar uma política de Criação de log a esse servidor de integração (consulte [Visualizando os logs para os servidores de integração ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/viewing-logs-for-your-integration-servers-in-app-connect-enterprise-beta)).
-   Localize respostas para perguntas comuns sobre o {{site.data.keyword.appconserviceshort}} em [Perguntas frequentes sobre o {{site.data.keyword.appconserviceshort}} ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://developer.ibm.com/integration/docs/app-connect/faq/).
-   Siga as instruções passo a passo sobre como conectar seus aplicativos nos [Tutoriais para o {{site.data.keyword.appconserviceshort}} ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/).
-   Se você tiver perguntas técnicas sobre como desenvolver ou implementar um aplicativo com o {{site.data.keyword.appconserviceshort}}, poste sua pergunta no [Stack Overflow ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](http://stackoverflow.com/search?q=app-connect+ibm-bluemix) e identifique sua pergunta com "ibm-bluemix" e "app-connect" (com um hífen).
-   Para perguntas sobre o serviço e instruções de introdução, use o fórum [IBM developerWorks&reg; dW Answers ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://developer.ibm.com/answers/topics/app_connect/?smartspace=bluemix). Inclua as tags "bluemix" e "app_connect" (com um sublinhado).

    Para obter mais informações sobre como usar os mecanismos de suporte do {{site.data.keyword.Bluemix}}, consulte [Obtendo ajuda ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://console.ng.bluemix.net/docs/support/index.html#getting-help).


