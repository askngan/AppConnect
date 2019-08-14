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


# IBM App Connect 문제점 해결
{: #troubleshooting}

{{site.data.keyword.appconservicefull}} 플로우 및 통합 서버의 문제점을 해결하기 위해 Kibana로 된 로그를 볼 수 있습니다. {{site.data.keyword.appconserviceshort}} 사용 중에 질문이나 문제점이 있는 경우 정보를 검색하거나 포럼을 통해 질문하여 도움을 받을 수 있습니다. 포럼을 사용하여 질문하는 경우 {{site.data.keyword.Bluemix}} 및 {{site.data.keyword.appconserviceshort}} 개발팀에서 볼 수 있도록 질문에 태그를 지정하십시오.

-   {{site.data.keyword.appconserviceshort}} 대시보드에서 실행 중인 플로우에 대한 타일을 살펴보십시오. 초록색의 체크 표시가 있으면 플로우가 성공적으로 실행 중인 것입니다. 플로우가 마지막으로 트리거된 시간을 확인하려면 체크 표시를 클릭하십시오. 

    ![플로우가 성공적으로 실행 중임을 보여주는 화면 캡처](/images/SuccessfulFlow.jpg)

    빨간색 느낌표가 있으면 문제점이 있는 것입니다. 문제점이 무엇인지 확인하려면 느낌표를 클릭하십시오. ![플로우에 문제점이 있음을 표시하는 화면 캡처](/images/ErroredFlow.jpg)

-   {{site.data.keyword.appconserviceshort}} 상태 페이지를 확인하여 보고된 문제가 있거나 유지보수가 계획되어 있는지 확인하십시오. [{{site.data.keyword.appconserviceshort}} 상태 페이지![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://developer.ibm.com/integration/docs/app-connect/app-connect-status/)
-   플로우에 대한 로그 정보를 보려면 {{site.data.keyword.appconserviceshort}} 메뉴에서 **로그**를 클릭하십시오. 기본적으로 플로우의 오류 및 정보 메시지는 Kibana로 표시됩니다. 여기서 특정 시간 범위의 데이터를 볼 수 있거나 필터를 사용하여 특정 유형의 정보를 볼 수 있습니다. 플로우에 대한 디버깅 정보를 보려면 {{site.data.keyword.appconserviceshort}} 대시보드의 플로우 타일에 있는 메뉴를 연 후 **디버그 로깅 사용**을 선택하십시오.  그런 다음 시작할 디버그 로깅에 대한 플로우를 다시 시작해야 합니다. 디버그 로깅을 사용으로 설정하면 디버그 로그 항목(잠재적으로 페이로드 데이터 포함)이 IBM 운영자에게 표시됩니다. 디버그 로깅에 대해 자세히 알아보려면 [{{site.data.keyword.appconserviceshort}}에서 메시지 플로우 디버깅![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/debugging-message-flows-ibm-app-connect/)을 참조하십시오. Kibana에 대해 자세히 알아보려면 [Kibana 문서 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://www.elastic.co/guide/en/kibana/4.0/discover.html)를 참조하십시오.
-   통합 서버에 대한 로그 정보를 보려면 통합 서버를 열고 **로그 다운로드** 또는 **로그 보기**를 클릭하십시오.  Kibana에서 통합 서버에 대한 로그를 보려면 로깅 정책을 해당 통합 서버에 첨부해야 합니다([통합 서버에 대한 로그 보기![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/viewing-logs-for-your-integration-servers-in-app-connect-enterprise-beta) 참조). 
-   [{{site.data.keyword.appconserviceshort}}에 대한 자주 묻는 질문 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://developer.ibm.com/integration/docs/app-connect/faq/)에서 {{site.data.keyword.appconserviceshort}}에 대한 일반적인 질문의 답을 찾을 수 있습니다.
-   [{{site.data.keyword.appconserviceshort}}의 튜토리얼 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/)에서 애플리케이션 연결 방법에 대한 단계별 지시사항을 따르십시오.
-   서비스 및 시작하기 지시사항에 대한 질문이 있는 경우 [IBM dW Answers![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://developer.ibm.com/answers/topics/app_connect) 포럼을 사용하십시오. "ibm_cloud" 및 "app_connect" 태그(밑줄 포함)를 포함하십시오. 

    {{site.data.keyword.Bluemix}} 지원 메커니즘 사용에 대한 자세한 정보는 [지원![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://cloud.ibm.com/unifiedsupport/supportcenter)을 참조하십시오. 

## IBM App Connect 팀에 문제점 보고
{: #reporting}

문제점 해결 어드바이스를 따랐는데도 문제점이 계속 발생하는 경우에는 {{site.data.keyword.appconserviceshort}} 팀으로부터 도움을 받을 수 있습니다. {{site.data.keyword.appconserviceshort}} 메뉴에서 **문의**를 클릭한 후 **지원 받기**를 클릭하십시오. IBM ID로 로그인하여 **케이스 작성**을 클릭한 후 다음과 같은 정보를 가능한 한 많이 제공하십시오. ({{site.data.keyword.Bluemix}} 콘솔에서 **지원**을 클릭할 수도 있습니다.) 

* {{site.data.keyword.appconserviceshort}}의 인스턴스가 프로비저닝되는 {{site.data.keyword.Bluemix}} 지역. (예: 댈러스 또는 런던)
* 사용 중인 {{site.data.keyword.appconserviceshort}} 서비스의 인스턴스 ID. ({{site.data.keyword.appconserviceshort}} 인스턴스 ID 아래의 계정 정보를 확인하여 이 ID를 찾을 수 있습니다.)
* 발생하고 있는 문제점. (예: 문제점이 특정 애플리케이션 또는 기능에 대한 문제점인지 여부)
* 문제점이 일괄처리와 관련된 경우 일괄처리 ID. (일괄처리 프로세스에서 오류가 발생하는 경우 일괄처리 프로세스의 각 레코드에 대해 ID를 정의했으면 Kibana 로그의 "batch-record-id_str" 열에서 정의된 ID를 찾을 수 있습니다. [{{site.data.keyword.appconserviceshort}}에서 일괄처리를 사용하는 방법![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://developer.ibm.com/integration/docs/app-connect/toolbox-utilities/how-to-use-batch-processing-in-ibm-app-connect/)을 참조하십시오.)
* 문제점이 처음 발생한 날짜 및 시간(시간대 포함)과 문제점이 발생하기 전에 플로우가 실행된 기간
* 문제점이 여전히 발생하고 있는지 여부 및 문제점을 복제할 수 있는지 여부
* 해당되는 경우 사용 중인 브라우저 유형 및 버전. (최신 브라우저 버전만 지원합니다.)
* 문제점을 설명하는 로그 항목
* 문제점이 비즈니스에 미치는 영향
