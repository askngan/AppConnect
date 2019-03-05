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


# Conceitos do IBM App Connect
{: #concepts}

O {{site.data.keyword.appconservicefull}} é uma ferramenta aliada dos negócios que pode ser usada para
integrar os aplicativos baseados em nuvem ou no local para automatizar as tarefas entediantes e repetitivas.

O {{site.data.keyword.appconserviceshort}} conecta seus aplicativos em minutos, automatizando atualizações,
notificações e eventos e mantendo seus dados em sincronização entre múltiplos aplicativos. É possível usá-lo para
conectar aplicativos na nuvem ou locais (no local).  

Há dois tipos de recursos que podem ser executados no {{site.data.keyword.appconserviceshort}} para conectar
seus aplicativos, dependendo de suas necessidades de negócios: servidores e fluxos de integração.  Para executar as soluções do IBM Integration Bus ou do App Connect Enterprise no {{site.data.keyword.appconserviceshort}}, faça upload de uma solução de integração em um arquivo BAR e, em seguida, execute-o em um servidor de integração no {{site.data.keyword.appconserviceshort}}.  Crie fluxos no {{site.data.keyword.appconserviceshort}} para conectar seus aplicativos para que algo
que aconteça em um aplicativo faça com que outra coisa aconteça em outro aplicativo. É possível criar fluxos acionados por evento e fluxos para APIs.

É possível usar o painel do {{site.data.keyword.appconserviceshort}} para monitorar os fluxos e os servidores
de integração para ver quanto trabalho eles estão fazendo. Inicie-os, pare-os e mude-os quando precisar.

Aqui vamos explicar os recursos e a terminologia do {{site.data.keyword.appconserviceshort}}:

-   [Fluxos](#flows)
-   [Aplicativos](#apps)
-   [Ações](#actions)
-   [Mapeamento de dados](#transforms)
-   [Arquivos BAR e servidores de integração](#barfiles)

## Fluxos
{: #flows}

Existem dois tipos de fluxo que podem ser criados no {{site.data.keyword.appconserviceshort}}: um fluxo acionado por evento e um fluxo para uma API.

Em um fluxo acionado por evento, você identifica um evento que pode ocorrer no primeiro aplicativo (o aplicativo de origem) e as ações que podem ser executadas em um ou mais aplicativos de destino. O fluxo vincula o evento às ações para que, sempre que o evento ocorra no aplicativo de origem, a ação seja acionada automaticamente nos aplicativos de destino. Cada ação concluída com sucesso conta para a sua cota mensal. Ao criar um fluxo, você inclui os aplicativos e escolhe as ações. Em seguida, mapeia os dados que deseja transferir entre os aplicativos.

Por exemplo, você pode criar um fluxo para que, sempre que
alguém se registrar como um novo participante com o Eventbrite (o evento), o {{site.data.keyword.appconserviceshort}} recupere automaticamente os detalhes do participante do Salesforce e crie uma nova tarefa no Asana (as ações).

![Um fluxo de multinós com o aplicativo de origem e dois aplicativos de destino](images/multi_node_flow2.jpg)

Para obter mais informações, consulte [Criando um fluxo acionado por evento ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/creating-event-driven-flow/).

Um fluxo para uma API contém uma solicitação, uma ou mais ações do aplicativo de destino e uma resposta. A solicitação usa um modelo que você define para solicitar a criação, a substituição ou a recuperação de objetos de dados nos aplicativos. Quando a solicitação é enviada, cada aplicativo de destino executa sua ação e, em seguida, o fluxo retorna uma resposta que confirma que as ações foram bem-sucedidas ou retorna os dados que foram solicitados.

![Um fluxo para uma API que cria um produto no Salesforce](images/APIFlow2.jpg)

Para obter mais informações, consulte [Criando fluxos para uma API ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/creating-flows-api/).

Além de incluir aplicativos em seus fluxos, também é possível incluir nós por meio da guia **Lógica**, que permite que você configure como os dados são processados. Porexemplo, use o nó Se para incluir algum processamento condicional executando diferentes ações de acordo com os dados que você receber (consulte [Incluindo lógica condicional em um fluxo ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/adding-conditional-logic-flow/)). Useo nó Para cada quando desejar executar uma ação para cada registro retornado por uma ação de recuperação (consulte [Recuperando itens dos aplicativos ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/using-ibm-app-connect-retrieve-items-applications/)).

Se você for um desenvolvedor do IBM Integration Bus ou do App Connect Enterprise, também será possível criar soluções de integração complexas desenvolvendo fluxos de mensagens no Kit de ferramentas de integração e empacotando-os em arquivos BAR.

Seus fluxos e servidores de integração são representados por blocos no painel do App Connect. Os blocos mostram as informações de resumo sobre o fluxo, a API ou o servidor de integração, tais como se um fluxo está em execução ou interrompido e se foi executado com êxito ou se produziu um erro. É possível clicar nos ícones de ponto de exclamação e de marcação para ver quando o fluxo foi executado com êxito pela última vez ou quais erros foram levantados. Clique nos três pontos ![O ícone de três pontos verticais abre um menu para iniciar, parar, editar ou excluir o fluxo](images/Menu.jpg) para abrir um menu que permite iniciar, parar, editar ou excluir seus recursos. Os fluxos precisam ser interrompidos antes que você possa editá-los.

![Captura de tela que mostra os blocos do painel para os fluxos acionados por evento, os fluxos para APIs e os servidores de integração](images/Dashboard.jpg)

## Aplicativos
{: #apps}

Ao criar fluxos acionados por evento ou fluxos para APIs, os _aplicativos_ são os aplicativos de software baseados em nuvem que você está conectando. É possível ver uma lista dos aplicativos aos quais você pode se conectar com o {{site.data.keyword.appconserviceshort}} na página **Aplicativos**. Clique em um aplicativo para descobrir mais sobre ele, para ver quais eventos e ações são suportados e para se conectar à sua própria conta. É possível ter múltiplas contas conectadas a cada aplicativo e alternar entre elas na página Aplicativos. Depois de ter se conectado à sua conta, também é possível atualizar ou remover a conta nessa página.

![Captura de tela de um dos aplicativos na página Aplicativos](images/Magento2.jpg)

Você não precisa se conectar a seus aplicativos na página Aplicativo, também pode se conectar no editor de fluxo à medida que incluir os aplicativos no fluxo. Muitos aplicativos requerem apenas um nome de usuário e uma senha, mas alguns precisam de mais informações. É possível descobrir como localizar essas informações nos [Guias de instruções para aplicativos ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://developer.ibm.com/integration/docs/app-connect/how-to-guides-for-apps/).

Se você estiver usando o {{site.data.keyword.appconservicefull}} para executar as soluções Enterprise Bus ou App Connect Enterprise na nuvem, um _aplicativo_ será o contêiner que retém seus fluxos de mensagens, bibliotecas e outros recursos que são requeridos pela solução. 

## Ações
{: #actions}

É possível incluir vários tipos de ação nos fluxos. As ações comuns são criar, recuperar e atualizar ou criar, mas alguns aplicativos têm ações específicas. Por exemplo, o aplicativo Lucy da Equals 3 tem uma ação chamada "Perguntar à Lucy" e o aplicativo Watson Personality Insights tem uma ação chamada "Analisar a personalidade". É possível ver uma lista de ações que são suportadas para aplicativos no {{site.data.keyword.appconserviceshort}} digitando o tipo de ação no campo de procura na parte superior da página Aplicativos:

![Captura de tela mostrando as ações de recuperação suportadas para os aplicativos](images/RetrieveApps2.jpg)

**Criar**

Como o nome sugere, a ação de criação cria um objeto ou um registro em um aplicativo. Por exemplo, se alguém se inscrever em seu evento ou enviar um formulário preenchido, talvez você queira criar um registro para essa pessoa no seu aplicativo de CRM ou de marketing. Ou, se uma pessoa abrir um chamado no aplicativo de help desk, talvez você queira criar um e-mail ou uma mensagem instantânea para assegurar que alguém trate dele imediatamente. Se houver uma possibilidade de que o objeto que você deseja criar já possa existir, será possível usar uma ação de *atualização ou criação* no lugar.

Para alguns aplicativos, talvez seja necessário fornecer algumas informações extras ao incluir uma ação de criação em um fluxo para que ele saiba em que local criar o objeto. Por exemplo, se você estiver usando um aplicativo de gerenciamento de projeto, como o Asana ou o Trello, ao criar uma tarefa ou uma placa, será necessário especificar o projeto ou a placa na qual você deseja incluí-la.

**Atualizar ou criar**

A ação de atualização ou criação mudará um registro existente em seu aplicativo de destino, se ele existir, mas criará o registro se ele ainda não existir. Ela também é conhecida como uma ação upsert (atualização ou inserção).

Por exemplo, digamos que alguém enviou um formulário do Wufoo com uma mudança de endereço. Se o contato já estiver em seu sistema CRM, você desejará atualizar seu endereço; mas, se ele não estiver, você desejará incluí-lo. Como a ação de recuperação, ao escolher uma ação para atualizar dados em um de seus aplicativos, é possível incluir uma ou mais condições para assegurar que você esteja atualizando as informações corretas.

Se houver mais de um registro em seu sistema de destino que corresponda aos seus critérios, você verá um erro para o fluxo no painel e o fluxo não atualizará nem criará nenhum registro. Por exemplo, talvez você tenha mais de um contato com o mesmo nome e sobrenome. Assim, você pode tentar corresponder a um contato usando dados exclusivos, como seu endereço de e-mail.

Os códigos de status que você provavelmente verá em resposta a uma ação de atualização ou de criação são:

-   200: Um registro foi atualizado
-   201: Um registro foi criado

É possível usar esses códigos de resposta posteriormente no fluxo. Talvez você queira executar ações diferentes, dependendo de se um registro foi atualizado ou criado. Para ver um exemplo de definição de ações com base em códigos de resposta, consulte o tutorial [Criando um fluxo acionado por evento que atualizará ou criará um contato no Salesforce e atualizará o Asana sempre que você receber um formulário no Wufoo](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/creating-event-driven-flow-updates-creates-contact-salesforce-updates-asana-whenever-receive-form-wufoo/).

**Recuperar**

A ação de recuperação obtém informações de um aplicativo para que você possa utilizá-las em outro aplicativo.

Ao incluir uma ação no fluxo para recuperar objetos, é possível definir uma ou mais condições para certificar-se de que esteja recuperando os itens corretos. Ou, se você apenas desejar recuperar todos os itens de um tipo específico, poderá excluir a condição. Também é possível definir quantos itens você deseja recuperar e o que acontecerá se o {{site.data.keyword.appconserviceshort}} localizar mais ou menos do que esse número.

É possível manipular seus itens recuperados de duas maneiras:

-   É possível incluir um nó "Para cada" após a ação de recuperação para executar uma ação para cada um dos itens que foram recuperados.
-   É possível incluir outra ação após a ação de recuperação para processar a lista de itens recuperados. Essa é uma ação única, independentemente de quantos itens sejam retornados, tais como a criação de um e-mail que lista todos os itens recuperados.

Também é possível decidir qual ação tomar com base no código de status que você obtém em resposta à ação de recuperação. Você poderia usar um nó "Se" para executar diferentes ações para diferentes códigos de status. Os códigos de status que você provavelmente verá em resposta a uma ação de recuperação são:

-   204: Nenhum registro foi localizado
-   200: Todos os registros no aplicativo correspondem à condição
-   206: O número máximo especificado de registros foi recuperado, mas existem mais registros correspondentes no aplicativo

Para obter mais informações, consulte [Recuperando itens dos aplicativos](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/using-ibm-app-connect-retrieve-items-applications/).

## Mapeamento de dados
{: #transforms}

Após criar um fluxo, incluir os aplicativos e selecionar as ações apropriadas, é necessário especificar quais informações deseja transferir entre os aplicativos. Você verá no editor de fluxo que ao incluir uma ação no fluxo, você vê uma lista de campos disponíveis para esse aplicativo, que podem ser preenchidos com dados do seu aplicativo de origem ou ações anteriores no fluxo.

Alguns campos são obrigatórios e estão marcados com um asterisco. Por exemplo, quando você está criando uma oportunidade de vendas no Salesforce, deve-se especificar um sobrenome:

![Captura de tela mostrando que o campo Sobrenome é obrigatório](images/LastName.jpg)

Ao clicar em um desses campos, você verá dois ícones: **Inserir referência**![Ícone Inserir referência](images/InsertRef.jpg) e **Aplicar uma função**![Ícone Aplicar uma função](images/Functions.jpg). Se você clicar em **Inserir referência**, você verá os dados disponíveis que podem ser colocados nesse campo de aplicativos anteriores no fluxo. O exemplo a seguir mostra que podemos escolher campos do aplicativo de origem Wufoo ou de uma ação anterior do Salesforce no fluxo. Também é possível usar o código de status por meio da ação de atualização ou de criação do Salesforce.

![Captura de tela mostrando as entradas disponíveis para um mapeamento de dados](images/Inputs.jpg)

No exemplo a seguir, nosso fluxo é acionado por um novo formulário preenchido que está sendo recebido no Wufoo. Queremos criar um contato no Salesforce para a pessoa que enviou o formulário. Então, quando incluímos a ação "Criar contato" do Salesforce ao fluxo, copiamos os detalhes para o nosso contato do formulário do Wufoo. Aqui podemos ver que, para o sobrenome do contato do Salesforce, selecionamos o sobrenome do requisitante do formulário do Wufoo. É possível ver que o campo mapeado é do Wufoo por causa da cor:

![Captura de tela mostrando que o campo Sobrenome do Wufoo é mapeado para o campo Sobrenome do Salesforce](images/Mapping.jpg)

No exemplo a seguir, incluímos uma ação "Criar mensagem" do Slack no fluxo após uma ação "Atualizar ou criar contato" do Salesforce. Nós simplesmente desejamos colocar uma mensagem no Slack para dizer qual código de resposta foi recebido para a ação do Salesforce:

![Captura de tela de uma ação Criar mensagem do Slack que mapeia um código de resposta](images/SlackSC.jpg)

É possível ver que no campo **Texto** para a ação "Criar mensagem" do Slack, digitamos uma mensagem e, em seguida, mapeamos no código de status para a ação "Atualizar ou criar contato" do Salesforce.

Aqui está outro exemplo de mapeamento de códigos de resposta de uma maneira diferente. Desta vez, incluímos um nó "Se" após uma ação "Atualizar ou criar contato" do Salesforce porque desejamos executar diferentes ações, dependendo de se um contato existente do Salesforce foi atualizado ou se um novo contato foi criado. Nesse caso, um código de resposta de "200" significa que o contato foi atualizado. Portanto, essa ramificação do nó "Se" conterá uma ação específica para um registro atualizado.

![Captura de tela mostrando os códigos de resposta sendo usados em um nó Se](images/IfSC.jpg)

O ícone **Aplicar uma função** ![Ícone Aplicar uma função](Functions.jpg) mostra uma lista de funções de transformação que podem ser usadas para customizar os dados que você está passando através do fluxo. Essas funções podem ser tão simples quanto converter um determinado campo em maiúsculas ou minúsculas ou um pouco mais complexas, como localizar e substituir padrões específicos nos dados. Elas também podem ser tão poderosas quanto formar expressões comuns. É possível selecionar a função que deseja na lista ou digitá-la você mesmo. A sintaxe das funções é JSONata, uma linguagem leve de consulta e transformação. Para obter mais informações, consulte [http://jsonata.org](http://jsonata.org).


## Arquivos BAR e servidores de integração
{: #barfiles}

Um arquivo BAR é um arquivo compactado para o qual você inclui recursos implementáveis no IBM Integration Bus ou no App Connect Enterprise. Ao desenvolver uma solução de integração no Integration Bus ou no App Connect Enterprise, empacote seus fluxos de mensagens e todos os recursos que esses fluxos de mensagens usam em um arquivo BAR e, em seguida, implemente o arquivo BAR em um servidor de integração. Esse servidor pode estar no local ou no {{site.data.keyword.appconserviceshort}}. É possível executar suas soluções Integration Bus ou App Connect Enterprise no App Connect, sem a necessidade de adquirir e manter uma infraestrutura de TI. Ao fazer upload de um arquivo BAR para o App Connect, um servidor de integração será criado para executar os conteúdos do arquivo BAR. É possível configurar a autenticação básica e a conectividade segura entre seus recursos baseados em nuvem e no local (consulte [Executando suas soluções Integration Bus no App Connect ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan)).  
