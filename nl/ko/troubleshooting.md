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


# IBM App Connect 문제점 해결
{: #troubleshooting}

{{site.data.keyword.appconservicefull}} 플로우 및 통합 서버의 문제점을 해결하기 위해 Kibana로 된 로그를 볼 수 있습니다. {{site.data.keyword.appconserviceshort}} 사용 중에 질문이나 문제점이 있는 경우 정보를 검색하거나 포럼을 통해 질문하여 도움을 받을 수 있습니다. 포럼을 사용하여 질문하는 경우 {{site.data.keyword.Bluemix}} 및 {{site.data.keyword.appconserviceshort}} 개발팀에서 볼 수 있도록 질문에 태그를 지정하십시오. 

-   {{site.data.keyword.appconserviceshort}} 대시보드에서 실행 중인 플로우에 대한 타일을 살펴보십시오. 초록색의 체크 표시가 있으면 플로우가 성공한 것입니다. 플로우가 마지막에 트리거된 시간을 확인하려면 체크 표시를 클릭하십시오. 

    ![플로우가 성공적으로 실행되었음을 표시하는 스크린샷](/images/SuccessfulFlow.jpg)

    빨간색의 느낌표가 있으면 문제점이 있는 것입니다. 문제점이 무엇인지 확인하려면 느낌표를 클릭하십시오. ![플로우에 문제점이 있음을 표시하는 스크린샷](/images/ErroredFlow.jpg)

-   {{site.data.keyword.appconserviceshort}} 상태 페이지를 클릭하여 현재 알려진 문제가 있거나 유지보수가 계획되어 있는지 확인하십시오. [{{site.data.keyword.appconserviceshort}} 상태 페이지 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://developer.ibm.com/integration/docs/app-connect/app-connect-status/)
-   플로우에 대한 로그 정보를 보려면 {{site.data.keyword.appconserviceshort}} 햄버거 메뉴의 **로그**를 클릭하십시오. 기본적으로 플로우의 오류 및 정보 메시지는 Kibana로 표시됩니다. 여기서 특정 시간 범위의 데이터를 볼 수 있거나 필터를 사용하여 특정 유형의 정보를 볼 수 있습니다. 플로우에 대한 디버깅 정보를 보려면 {{site.data.keyword.appconserviceshort}} 대시보드의 플로우 타일에 있는 메뉴를 연 후 **디버그 로깅 사용**을 선택하십시오. 그런 다음 시작할 디버그 로깅에 대한 플로우를 다시 시작해야 합니다. 디버그 로깅을 사용으로 설정할 때 디버그 로그 항목(잠재적으로 페이로드 데이터 포함)은 IBM 운영자에게 표시됩니다. 디버그 로깅에 대해 자세히 알아보려면 [{{site.data.keyword.appconserviceshort}}에서 메시지 플로우 디버깅](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/debugging-message-flows-ibm-app-connect/)을 참조하십시오. Kibana에 대해 자세히 알아보려면 [Kibana 문서 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://www.elastic.co/guide/en/kibana/4.0/discover.html)를 참조하십시오.
-   통합 서버에 대한 로그 정보를 보려면 통합 서버를 열고 **로그 다운로드** 또는 **로그 보기**를 클릭하십시오. Kibana로 표시된 통합 서버의 로그를 보려면 로깅 정책을 해당 통합 서버에 첨부해야 합니다([통합 서버에 대한 로그 보기 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/viewing-logs-for-your-integration-servers-in-app-connect-enterprise-beta) 참조).
-   [{{site.data.keyword.appconserviceshort}}에 대한 자주 묻는 질문 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://developer.ibm.com/integration/docs/app-connect/faq/)에서 {{site.data.keyword.appconserviceshort}}에 대한 일반적인 질문의 답을 찾을 수 있습니다.
-   [{{site.data.keyword.appconserviceshort}}의 튜토리얼 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/)에서 애플리케이션 연결 방법에 대한 단계별 지시사항을 따르십시오. 
-   {{site.data.keyword.appconserviceshort}}에서의 애플리케이션 개발 또는 배치에 대한 기술 질문이 있는 경우 [스택 오버플로우 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](http://stackoverflow.com/search?q=app-connect+ibm-bluemix)에 질문을 게시하고 "ibm-bluemix" 및 "app-connect"(하이픈 사용)로 질문에 태그를 지정하십시오. 
-   서비스 및 시작하기 지시사항에 대한 질문은 [IBM developerWorks&reg; dW Answers ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://developer.ibm.com/answers/topics/app_connect/?smartspace=bluemix) 포럼을 사용하십시오. "bluemix" 및 "app_connect"(밑줄 사용) 태그를 포함하십시오.

    {{site.data.keyword.Bluemix}} 지원 메커니즘 사용에 대한 자세한 정보는 [도움 받기 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://console.ng.bluemix.net/docs/support/index.html#getting-help)를 참조하십시오.


