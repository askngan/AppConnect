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


# IBM App Connect 개념
{: #concepts}

{{site.data.keyword.appconservicefull}}는 비즈니스 친화적인 도구로, 지루하고 반복적인 태스크를 자동화하도록 클라우드 기반 또는 온프레미스 애플리케이션을 통합하는 데 사용할 수 있습니다.

다음은 {{site.data.keyword.appconserviceshort}}의 기능 및 용어입니다. 

-   [플로우](#flows)
-   [애플리케이션](#apps)
-   [조치](#actions)
-   [데이터 맵핑](#transforms)
-   [BAR 파일 및 통합 서버](#barfiles)

## 플로우
{: #flows}

{{site.data.keyword.appconserviceshort}}에서 작성할 수 있는 두 가지 유형의 플로우 즉, 이벤트 중심 플로우 및 API용 플로우가 있습니다.

이벤트 중심 플로우에서 첫 번째 애플리케이션(소스 애플리케이션)에서 발생할 수 있는 이벤트와 하나 이상의 대상 애플리케이션에서 수행될 수 있는 조치를 식별합니다. 플로우는 이벤트가 소스 애플리케이션에서 발생할 때마다 조치가 대상 애플리케이션에서 자동으로 트리거되도록 이벤트를 조치에 연결합니다. 완료된 각 조치는 매달 할당량에 포함됩니다. 플로우를 작성하는 경우 애플리케이션을 추가하고 조치를 선택합니다. 그런 다음 애플리케이션 간에 전송할 데이터를 맵핑합니다.

예를 들어, Eventbrite(이벤트)를 사용하여 새 참석자로 등록할 때마다 {{site.data.keyword.appconserviceshort}}가 Salesforce에서 참석자의 세부사항을 자동으로 검색하고 Asana(조치)에서 새 태스크를 작성하도록 플로우를 작성할 수 있습니다.

![소스 애플리케이션 및 두 개의 대상 애플리케이션이 포함된 다중 노드 플로우](images/multi_node_flow2.jpg)

자세한 정보는 [이벤트 중심 플로우 작성 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/creating-event-driven-flow/)을 참조하십시오.

API용 플로우에는 요청, 하나 이상의 대상 애플리케이션 조치 및 응답이 포함되어 있습니다. 요청은 애플리케이션에서 데이터 오브젝트의 작성, 대체 또는 검색을 요청하기 위해 정의하는 모델을 사용합니다. 요청이 제출되는 경우 각 대상 애플리케이션은 해당 조치를 수행하고, 그런 다음 플로우는 조치가 성공적이었음을 확인하거나 요청된 데이터를 리턴하는 응답을 리턴합니다. 

![Salesforce에서 제품을 작성하는 API용 플로우](images/APIFlow2.jpg)

자세한 정보는 [API용 플로우 작성 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/creating-flows-api/)을 참조하십시오.

애플리케이션을 플로우에 추가하는 것 외에도, 데이터 처리 방법을 구성할 수 있도록 하는 **로직** 탭에서 노드를 추가할 수도 있습니다. 예를 들어, If 노드를 사용하여 수신하는 데이터에 따라 다른 조치를 수행하도록 일부 조건부 처리를 추가하십시오([플로우에 조건부 로직 추가 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/adding-conditional-logic-flow/) 참조). 또한 검색 조치로 리턴되는 각 레코드에 조치를 수행하려고 할 때 For each 노드를 사용하십시오([애플리케이션에서 항목 검색 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/using-ibm-app-connect-retrieve-items-applications/) 참조).

IBM Integration Bus 또는 App Connect Enterprise 개발자인 경우 Integration Toolkit에서 메시지 플로우를 개발하고 메시지 플로우를 BAR 파일로 패키지하여 복합 통합 솔루션도 작성할 수 있습니다. 

플로우 및 통합 서버는 App Connect 대시보드에서 타일로 표시됩니다. 타일에 플로우, API 또는 통합 서버에 대한 정보를 요약합니다(예: 플로우가 실행 중인지 또는 중지되었는지 여부, 성공적으로 실행되었는지 또는 오류가 발생했는지 여부). 체크 표시 및 느낌표 아이콘을 클릭하여 플로우가 마지막에 성공적으로 실행된 시간 또는 발생한 오류를 확인할 수 있습니다. 세 개의 점 ![수직으로 된 세 개의 점 아이콘이 플로우를 시작, 중지, 편집 또는 삭제하기 위해 열림](images/Menu.jpg)을 클릭하여 리소스를 시작, 중지, 편집 또는 삭제할 수 있는 메뉴를 여십시오. 플로우를 편집하려면 플로우를 중지해야 합니다. 

![이벤트 중심 플로우, API용 플로우 및 통합 서버를 위해 대시보드에서 타일을 표시하는 스크린샷](images/Dashboard.jpg)

## 애플리케이션
{: #apps}

이벤트 중심 플로우 또는 API용 플로우를 작성하는 경우 _애플리케이션_은 연결 중인 클라우드 기반 소프트웨어 애플리케이션입니다. **애플리케이션** 페이지에서 {{site.data.keyword.appconserviceshort}}와 연결할 수 있는 애플리케이션의 목록을 볼 수 있습니다. 애플리케이션을 클릭하여 세부사항을 알아보고, 지원되는 이벤트 및 조치를 확인하고, 고유 계정에 연결하십시오. 각 애플리케이션에 연결된 여러 개의 계정을 보유하고 애플리케이션 페이지에서 이 계정 간에서 전환할 수 있습니다. 계정에 연결한 후 이 페이지에서 계정을 업데이트하거나 제거할 수도 있습니다. 

![애플리케이션 페이지에 있는 애플리케이션의 스크린샷](images/Magento2.jpg)

애플리케이션 페이지에서 애플리케이션에 연결할 필요가 없습니다. 애플리케이션을 플로우에 추가할 때 플로우 편집기에서 연결할 수도 있습니다. 많은 애플리케이션에는 사용자 이름 및 비밀번호만이 아닌 일부 추가 정보가 필요합니다. [앱 사용 방법 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://developer.ibm.com/integration/docs/app-connect/how-to-guides-for-apps/)에서 이 정보를 찾는 방법을 확인할 수 있습니다. 

{{site.data.keyword.appconservicefull}}를 사용하여 클라우드에서 Integration Bus 또는 App Connect Enterprise 솔루션을 실행하는 경우 _애플리케이션_은 솔루션에 필요한 메시지 플로우, 라이브러리 및 기타 리소스를 보유하고 있는 컨테이너입니다. 

## 조치
{: #actions}

여러 유형의 조치를 플로우에 추가할 수 있습니다. 공통 조치는 작성, 검색 및 업데이트 또는 작성이지만 일부 애플리케이션에는 특정 조치가 있습니다. 예를 들어, Equals 3 Lucy 애플리케이션에는 "Ask Lucy"라고 하는 조치가 있고 Watson Personality Insights 애플리케이션에는 "Analyze personality"라고 하는 조치가 있습니다. 애플리케이션 페이지의 상단에 있는 검색 필드에 조치 유형을 입력하여 {{site.data.keyword.appconserviceshort}}의 애플리케이션에 지원되는 조치의 목록을 볼 수 있습니다. 

![애플리케이션을 위해 지원되는 검색 조치를 표시하는 스크린샷](images/RetrieveApps2.jpg)

**작성**

이름에서 알 수 있듯이 작성 조치는 애플리케이션에서 오브젝트 또는 레코드를 작성합니다. 예를 들어, 누군가가 이벤트에 가입하거나 완료된 양식을 제출하는 경우 CRM 또는 마케팅 애플리케이션에 해당 사용자에 대한 레코드를 작성하려고 할 수 있습니다. 또는 누군가가 헬프 데스크 애플리케이션에서 티켓을 여는 경우 해당 사용자가 즉시 처리하는지 확인하기 위해 이메일 또는 인스턴트 메시지를 작성하려고 할 수 있습니다. 작성하려는 오브젝트가 이미 존재하는 가능성이 있는 경우 *업데이트 또는 작성* 조치를 대신 사용할 수 있습니다. 

일부 애플리케이션의 경우, 플로우에서 오브젝트 작성 위치를 알 수 있도록 작성 조치를 플로우에 추가할 때 일부 추가 정보를 제공해야 할 수 있습니다. 예를 들어, Asana 또는 Trello와 같은 프로젝트 관리 애플리케이션을 사용 중인 경우 태스크 또는 카드를 작성할 때 이를 추가할 프로젝트 또는 게시판을 지정해야 합니다. 

**업데이트 또는 작성**

레코드가 존재하는 경우 업데이트 또는 작성 조치로 대상 애플리케이션의 기존 레코드가 변경되지만, 아직 존재하지 않는 경우에는 레코드가 작성됩니다. 업데이트삽입(upsert: 업데이트 또는 삽입) 조치라고도 합니다. 

예를 들어, 누군가가 주소를 변경하여 Wufoo 양식을 제출했습니다. CRM 시스템에 연락처가 이미 있는 경우 주소를 업데이트하려고 하지만 없는 경우 추가하려고 합니다. 검색 조치와 같이 사용자의 애플리케이션에서 데이터를 업데이트하도록 선택하는 경우 올바른 정보를 업데이트하고 있는지 확인하기 위해 하나 이상의 조건을 추가할 수 있습니다. 

사용자의 기준과 일치하는 대상 시스템에 둘 이상에 레코드가 있는 경우, 대시보드에 플로우 관련 오류가 표시되고 플로우는 레코드를 업데이트하거나 작성하지 않습니다. 예를 들어, 성 또는 이름이 같은 연락처가 두 개 이상 있을 수 있습니다. 그러므로 이메일 주소와 같이 고유 데이터를 사용하여 연락처를 일치시키도록 할 수 있습니다. 

업데이트 또는 작성 조치에 응답하여 볼 수 있는 상태 코드는 다음과 같습니다. 

-   200: 레코드가 업데이트되었음
-   201: 레코드가 작성되었음

나중에 플로우에서 이러한 응답 코드를 사용할 수 있습니다. 레코드가 업데이트되었는지 아니면 작성되었는지에 따라 다른 조치를 수행하려고 할 수 있습니다. 응답 코드에 기반한 조치 정의에 대한 예제는 [Wufoo 양식으로 수신할 때마다 Salesforce에서 연락처를 업데이트 또는 작성하고 Asana에서 연락처를 업데이트하는 이벤트 중심 플로우 작성](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/creating-event-driven-flow-updates-creates-contact-salesforce-updates-asana-whenever-receive-form-wufoo/) 튜토리얼을 참조하십시오.

**검색**

검색 조치는 애플리케이션에서 정보를 수집하여 다른 애플리케이션에서 정보를 사용할 수 있도록 합니다.

조치를 플로우에 추가하여 오브젝트를 검색하는 경우 올바른 항목을 검색하고 있는지 확인하기 위해 하나 이상의 조건을 정의할 수 있습니다. 또는 특정 유형의 모든 항목을 검색하려는 경우 조건을 삭제할 수 있습니다. 또한 검색할 항목 수와 {{site.data.keyword.appconserviceshort}}에서 해당 수를 초과하거나 미만임을 발견하는 경우 발생하는 사항도 정의할 수 있습니다. 

다음 두 가지 방법으로 검색된 항목을 처리할 수 있습니다. 

-   검색 조치 후 "For each" 노드를 추가하여 검색한 항목마다 조치를 수행할 수 있습니다. 
-   검색 조치 후 다른 조치를 추가하여 검색된 항목의 목록을 처리할 수 있습니다. 이는 단일 조치로, 검색된 모든 항목을 나열하는 이메일 작성과 같이 리턴되는 항목의 수와 관계가 없습니다. 

검색 조치에 응답하여 가져오는 상태 코드를 기반으로 취할 조치를 결정할 수도 있습니다. "If" 노드를 사용하여 다른 상태 코드에 다른 조치를 수행할 수 있습니다. 검색 조치에 응답하여 볼 수 있는 상태 코드는 다음과 같습니다. 

-   204: 레코드를 찾을 수 없음
-   200: 애플리케이션의 모든 레코드가 조건과 일치함
-   206: 지정된 최대 레코드 수가 검색되었으나 일치하는 레코드가 애플리케이션에 더 많이 존재합니다. 

자세한 정보는 [애플리케이션에서 항목 검색](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/using-ibm-app-connect-retrieve-items-applications/)을 참조하십시오.

## 데이터 맵핑
{: #transforms}

플로우를 작성하고, 애플리케이션을 추가하고, 적절한 조치를 선택한 경우 애플리케이션 간에 전송할 정보를 지정해야 합니다. 플로우 편집기에서 조치를 플로우에 추가하는 시간, 해당 애플리케이션의 사용 가능한 필드 목록, 소스 애플리케이션에서 데이터로 채울 수 있는 항목 또는 플로우의 이전 조치가 표시됩니다. 

일부 필드가 필수이며 별표로 표시됩니다. 예를 들어, Salesforce에서 리드를 작성하는 경우 성을 지정해야 합니다. 

![성 필드가 필수임을 표시하는 스크린샷](images/LastName.jpg)

이 필드 중 하나를 클릭하는 경우 **삽입 참조**![삽입 참조 아이콘](images/InsertRef.jpg) 및 **기능 적용**![기능 적용 아이콘](images/Functions.jpg)의 두 가지 아이콘이 표시됩니다. **삽입 참조**를 클릭하는 경우 플로우에서 선행하는 애플리케이션의 해당 필드에 입력할 수 있는 가능한 데이터가 표시됩니다. 다음 예제는 플로우의 Wufoo 소스 애플리케이션 또는 이전 Salesforce 조치에서 필드를 선택할 수 있음을 보여줍니다. Salesforce 업데이트 또는 작성 조치에서 상태 코드도 사용할 수 있습니다. 

![데이터 맵핑에 사용 가능한 입력을 표시하는 스크린샷](images/Inputs.jpg)

다음 예제에서 플로우는 Wufoo에서 수신되는 새로 완료된 양식으로 트리거됩니다. 양식을 제출한 사용자를 위해 Salesforce에 연락처를 작성하려고 합니다. 그러므로 Salesforce "연락처 작성" 조치를 플로우에 추가하는 경우 Wufoo 양식에서 연락처에 대한 세부사항을 복사합니다. 여기서 Salesforce 연락처의 성에 해당하는 항목이 표시되며 Wufoo 양식 제출자의 성을 선택했습니다. 다음과 같이 색상으로 인해 맵핑된 필드는 Wufoo에서 작성되었음을 확인할 수 있습니다. 

![Wufoo 성 필드가 Salesforce 성 필드에 맵핑됨을 표시하는 스크린샷](images/Mapping.jpg)

다음 예제에서 Salesforce "연락처 업데이트 또는 작성" 조치 후 슬랙 "메시지 작성" 조치를 플로우에 추가했습니다. 단지 Salesforce 조치에 대해 수신된 응답 코드를 표시하기 위해 메시지를 작성하려고 합니다. 

![응답 코드를 맵핑하는 슬랙 메시지 작성 조치의 스크린샷](images/SlackSC.jpg)

슬랙 "메시지 작성" 조치의 **텍스트** 필드에서 메시지를 입력한 후 Salesforce "연락처 업데이트 또는 작성" 조치를 위해 상태 코드에 맵핑했음을 확인할 수 있습니다. 

이는 다른 방식으로 수행된 맵핑 응답 코드의 또 다른 예제입니다. 이 때 기존 Salesforce 연락처가 업데이트되었거나 새 연락처가 작성되었는지 여부에 따라 다른 조치를 수행하려고 하므로 Salesforce "연락처 업데이트 또는 작성" 조치 후에 "If" 노드를 추가했습니다. 이 경우 "200" 응답 코드는 연락처가 업데이트되었음을 의미합니다. 그러므로 "If" 노드의 이 분기에는 업데이트된 레코드에 특정한 조치가 포함됩니다. 

![If 노드에 사용 중인 응답 코드를 표시하는 스크린샷](images/IfSC.jpg)

**기능 적용** 아이콘 ![기능 적용 아이콘](Functions.jpg)은 플로우를 통해 전달 중인 데이터를 사용자 정의하는 데 사용할 수 있는 변환 기능의 목록을 표시합니다. 이 기능은 특정 필드를 대문자 또는 소문자로 변환하는 만큼 간단하거나 데이터에서 특정 패턴 찾기 및 대체와 같이 약간 더 복잡할 수 있습니다. 또한 정규식을 구성하는 만큼 강력할 수 있습니다. 목록에서 원하는 기능을 선택하거나 스스로 입력할 수 있습니다. 기능의 구문은 JSONata로 경량 조회 및 변환 언어입니다. 자세한 정보는 [http://jsonata.org](http://jsonata.org)를 참조하십시오.


## BAR 파일 및 통합 서버
{: #barfiles}

BAR 파일은 IBM Integration Bus 또는 App Connect Enterprise에 배치 가능한 리소스를 추가하는 압축된 파일입니다. Integration Bus 또는 App Connect Enterprise에 통합 솔루션을 개발하는 경우 메시지 플로우 및 해당 메시지 플로우가 BAR 파일로 사용하는 모든 리소스를 패키지한 후 BAR 파일을 통합 서버에 배치합니다. 해당 서버는 온프레미스 또는 {{site.data.keyword.appconserviceshort}}에 있을 수 있습니다. IT 인프라를 확보하고 유지보수할 필요 없이 App Connect에서 Integration Bus 또는 App Connect Enterprise 솔루션을 실행할 수 있습니다. BAR 파일을 App Connect에 업로드하는 경우 통합 서버는 BAR 파일의 컨텐츠를 실행하도록 작성됩니다. 클라우드 기반 및 온프레미스 리소스 간에 기본 인증 및 보안 연결을 구성할 수 있습니다([App Connect에서 Integration Bus 솔루션 실행 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan) 참조).  
