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


# Introdução ao IBM App Connect
{: #getting-started}

O {{site.data.keyword.appconservicefull}} ajuda você a conectar seus aplicativos: desde simples interações
de ação acionadora até integrações complexas. É possível usar o {{site.data.keyword.appconserviceshort}} para
criar fluxos acionados por evento ou fluxos para APIs ou fazer upload e executar as soluções de integração criadas no IBM Integration Bus, sem a necessidade de adquirir
e manter uma infraestrutura de TI.  É possível ver e administrar todas as suas integrações (servidores de integração,
fluxos acionados por eventos e fluxos para APIs) em um local no painel do {{site.data.keyword.appconserviceshort}}. 

Depois de criar uma instância do serviço do {{site.data.keyword.appconserviceshort}}, é possível acessar o
{{site.data.keyword.appconserviceshort}} por meio do painel do {{site.data.keyword.Bluemix}}.

As etapas a seguir fornecem informações suficientes para que você inicie com o App Connect. Para obter
instruções mais detalhadas, guias de instruções para aplicativos específicos, tutoriais e vídeos, consulte o conjunto
completo de documentação em [IBM App Connect
![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://developer.ibm.com/integration/docs/app-connect/).

## Criando um fluxo acionado por evento

Conforme o nome sugere, um fluxo acionado por evento consiste em um evento em um aplicativo de origem que aciona o fluxo e em uma ou mais ações nos aplicativos de destino. Portanto, quando algo acontece no aplicativo de origem, uma ação é acionada nos aplicativos de destino. Para criar um fluxo acionado por evento que conecta seus aplicativos baseados em nuvem, conclua as etapas a seguir.
1.  No painel do {{site.data.keyword.appconserviceshort}}, clique em **Novo**>**Fluxo acionado por evento**. O {{site.data.keyword.appconserviceshort}} salva suas mudanças automaticamente à medida que você avança. Se você navegar para fora do fluxo em qualquer estágio, o fluxo será salvo como um fluxo de rascunho que você pode concluir em outro momento.
1.  Insira um nome para o fluxo.
1.  Selecione o evento acionador para iniciar o fluxo expandindo um aplicativo e selecionando um evento.
1.  Se você ainda não se conectou ao seu aplicativo, clique em **Conectar ao _aplicativo_** e insira os seus detalhes de login para o aplicativo.     Pode ser necessário fornecer detalhes adicionais de conexão para alguns aplicativos. Se você precisar de ajuda para localizar credenciais para um aplicativo específico, consulte os [Guias de instrução para aplicativos ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://developer.ibm.com/integration/docs/app-connect/how-to-guides-for-apps/).
1.  Selecione a ação a ser acionada em seu segundo aplicativo expandindo um aplicativo e selecionando uma ação. Se necessário, clique em **Conectar ao aplicativo** e insira os detalhes de login para o aplicativo de destino.
1. Insira os dados que você deseja transferir entre seus aplicativos.  É possível incluir manualmente os nomes de campo de origem clicando em um campo e, em seguida, clicando no ícone de mapeamento ![Ícone de mapeamento](/images/MappingIcon.jpg). Também é possível digitar texto ou usar uma função de transformação para customizar o valor de origem. Para obter mais informações, consulte [Como usar as transformações ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://developer.ibm.com/integration/docs/app-connect/faq/#faq_transforms).
1. Opcional: é possível refinar como seu fluxo funciona executando as ações a seguir:
    * Inclua mais aplicativos de destino e ações clicando no ícone de mais no fluxo ![Ícone Incluir um aplicativo](/images/AddApp.jpg).
    * Inclua ações de recuperação em seu fluxo para recuperar itens que correspondam a determinados critérios, recuperar um número especificado de registros, definir a manipulação de erros ou definir como manipular os itens que são recuperados (consulte [Usando o App Connect para recuperar itens de seus aplicativos ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/using-ibm-app-connect-retrieve-items-applications/)).
    * Inclua alguma lógica condicional para executar ações diferentes, dependendo dos dados que são recebidos de aplicativos em seu fluxo (consulte [Incluindo lógica condicional em um fluxo ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/adding-conditional-logic-flow/)).

1. Após ter configurado o fluxo, abra o menu de opções na barra de cabeçalho e clique em **Iniciar fluxo**.

Se você retornar para o painel do {{site.data.keyword.appconserviceshort}}, poderá ver o fluxo em execução. Quando um evento acontecer no primeiro aplicativo, uma ação será acionada automaticamente pelo {{site.data.keyword.appconserviceshort}} no segundo aplicativo. É possível visualizar o status dos fluxos no painel do {{site.data.keyword.appconserviceshort}}. Para visualizar logs para os fluxos, abra o menu hambúrguer ![Ícone do menu hambúrguer](/images/HamburgerMenuSm.jpg), expanda **Gerenciar** e, em seguida, clique em **Logs**.

Para obter informações mais detalhadas sobre a criação de fluxos acionados por evento, incluindo alguns exemplos, consulte [Criando um fluxo acionado por evento ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/creating-event-driven-flow/).

## Criando um fluxo para uma API

Se desejar que um desenvolvedor possa criar um aplicativo que use dos dados em seus aplicativos baseados em nuvem, será possível fornecer uma API. Para criar fluxos para uma API, conclua as etapas a seguir.
1. No painel do {{site.data.keyword.appconserviceshort}}, clique em **Novo** > **Fluxos para uma API**.
1. Insira um nome para a API.
1. Insira um nome para o modelo que reflita o tipo de objeto com o qual sua API trabalhará e, em seguida, clique em **Criar modelo**.
1. Inclua as propriedades que são necessárias para definir a estrutura do objeto com o qual a API trabalhará. Por exemplo, se a API criar ou recuperar um cliente, você poderá incluir propriedades chamadas Customer_ID, First_Name, Last_Name e Email_Address. É possível digitar o nome de uma propriedade ou clicar em **Selecionar propriedades de aplicativos** para escolher propriedades de um ou mais dos aplicativos aos quais você está conectado.
1. Clique em **Operações** para definir como a API interagirá com o objeto e inclua as operações necessárias. 
1. Para cada operação, clique em **Implementar fluxo** para criar um fluxo que define como cada operação funcionará. 
1. Inclua um ou mais aplicativos de destino no fluxo, entre a solicitação e a resposta. Se você desejar que o fluxo faça diferentes coisas para diferentes condições, também será possível incluir alguma lógica condicional (consulte [Incluindo a lógica condicional em um fluxo ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/adding-conditional-logic-flow/)).
1. Clique em **Resposta** no fluxo para definir a resposta que será retornada quando a operação tiver sido executada. Mapeie os campos disponíveis por meio do seu aplicativo de destino. 
1. Clique em **Pronto** para retornar ao modelo.
1. Quando você tiver definido todos os modelos e operações, inicie a API selecionando **Iniciar API** no menu. 

Você criou os fluxos para a API. No painel do {{site.data.keyword.appconserviceshort}}, os fluxos para APIs são identificados pelo ícone de API. É possível iniciá-los e pará-los da mesma maneira que qualquer outro fluxo. É possível abrir uma API enquanto ela está em execução, mas você tem que pará-la antes de poder editá-la.

Para obter informações mais detalhadas sobre como criar fluxos para APIs, incluindo exemplos, consulte [Criando fluxos para uma API ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/creating-flows-api/).

Para descobrir como testar a API, consulte [Expondo um fluxo do App Connect por meio da API Connect ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://developer.ibm.com/integration/blog/2017/08/29/exposing-app-connect-flow-api-connect/).


## Executando uma solução de integração do IBM Integration Bus (Enterprise Beta)

Se desejar implementar as soluções de integração que você desenvolveu no IBM Integration Bus ou no App Connect Enterprise para a nuvem, sem a necessidade de adquirir e manter uma infraestrutura de TI, será possível importar um arquivo BAR que contém todos os artefatos que compõem sua solução de integração e, em seguida, executar o conteúdo em um servidor de integração no App Connect. Para fazer upload de um arquivo BAR para o App Connect, deve-se ter o IBM Integration Bus versão 10.0.0.4 ou mais recente ou o App Connect Enterprise instalado no local.

Para executar as soluções do Integration Bus ou do App Connect Enterprise no App Connect, conclua as etapas a seguir.
1. No painel do {{site.data.keyword.appconserviceshort}}, clique em **Novo** > **Importar um arquivo BAR**.
1. Selecione o arquivo BAR que deseja importar, edite o nome, se desejar e, em seguida, clique em **Importar**. Se você vir um erro de autenticação, verifique se o seu arquivo BAR é válido (consulte [O que torna um arquivo BAR válido no App Connect? ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/what-makes-a-bar-file-valid-for-app-connect-app-connect-enterprise-beta)). Um servidor de integração é criado e um bloco é incluído no painel para representá-lo. O status será mudado de "Preparando" para "Interrompido" quando o servidor de integração estiver pronto para ser configurado e iniciado. 
1. Clique no bloco para abrir o servidor de integração.
1. Configure o servidor de integração:
    * Inclua ou edite uma descrição para a sua solução de integração.
    * Configure a autenticação básica HTTPS (consulte [Configurando a autenticação básica HTTPS ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/configuring-https-basic-authentication-app-connect-enterprise-beta)).
    * Anexe uma política para que seja possível conectar-se a sistemas locais (consulte [Configurando a conectividade segura entre os servidores de integração no App Connect e os sistemas no local ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/configuring-secure-connectivity-between-integration-servers-on-app-connect-and-on-premises-systems-app-connect-enterprise-beta)).
1. Opcional: para dividir o processamento de fluxo de mensagens entre seu ambiente local e o App Connect, configure os fluxos de chamada abrindo o menu hambúrguer ![Ícone do menu hambúrger](/images/HamburgerMenuSm.jpg), expandindo **Gerenciar**e selecionando **Fluxos de chamada** (consulte [Compartilhando o processamento de fluxo de mensagens entre o App Connect e o Integration Bus ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/sharing-message-flow-processing-between-app-connect-and-integration-bus-app-connect-enterprise-beta)).
1. Quando você tiver concluído a configuração, retorne ao painel do App Connect e inicie o servidor de integração abrindo o menu de bloco e clicando em **Iniciar**.

Quando o servidor de integração estiver em execução, será possível visualizar e fazer download de logs abrindo o servidor de integração e clicando em **Fazer download de logs** ou em **Visualizar logs**. Para visualizar os logs, é necessário anexar uma política de Criação de log em seu servidor de integração (consulte [Visualizando logs para os servidores de integração ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/viewing-logs-for-your-integration-servers-in-app-connect-enterprise-beta).)

Para obter informações mais detalhadas, consulte [Executando suas soluções do Integration Bus no App Connect ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan).
