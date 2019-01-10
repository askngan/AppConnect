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


# IBM App Connect 시작하기
{: #gettingStarted}

{{site.data.keyword.appconservicefull}}는 단순한 트리거-조치 상호작용에서 복잡한 상호작용까지 이르는 애플리케이션에 연결하는 데 도움을 줍니다. {{site.data.keyword.appconserviceshort}}를 사용하여 이벤트 중심 플로우 또는 API용 플로우를 작성할 수 있거나, IT 인프라를 확보하고 유지보수할 필요 없이 IBM Integration Bus에 작성하는 통합 솔루션을 실행할 수 있습니다. 모든 통합 즉, 통합 서버, 이벤트 중심 플로우 및 API용 플로우를 {{site.data.keyword.appconserviceshort}} 대시보드의 하나의 위치에서 보고 관리할 수 있습니다.  

{{site.data.keyword.appconserviceshort}} 서비스의 인스턴스를 작성한 후 {{site.data.keyword.Bluemix}} 대시보드에서 {{site.data.keyword.appconserviceshort}}에 액세스할 수 있습니다. 

다음 단계는 App Connect를 시작하는 데 충분한 정보를 제공합니다. 자세한 지시사항, 특정 애플리케이션, 튜토리얼 및 동영상에 대한 사용 방법은 [IBM App Connect ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://developer.ibm.com/integration/docs/app-connect/)에서 전체 문서 세트를 참조하십시오. 

## 이벤트 중심 플로우 작성

이름에서 알 수 있듯이 이벤트 중심 플로우는 소스 애플리케이션에서 플로우를 트리거하는 이벤트로 구성되고 대상 애플리케이션에서 하나 이상의 조치로 구성됩니다. 그러므로 소스 애플리케이션에서 어떠한 사항이 발생하면 조치가 대상 애플리케이션에서 트리거됩니다. 클라우드 기반 애플리케이션에 연결하는 이벤트 중심 플로우를 작성하려면 다음 단계를 완료하십시오.
1.  {{site.data.keyword.appconserviceshort}} 대시보드에서 **새로 작성** > **이벤트 중심 플로우**를 클릭하십시오.
    {{site.data.keyword.appconserviceshort}}는 이동 시 자동으로 변경사항을 저장합니다. 어떠한 단계에서든 플로우를 닫는 경우 플로우는 다른 시간에 완료할 수 있도록 임시 플로우로 저장됩니다. 
1.  플로우의 이름을 입력하십시오. 
1.  애플리케이션을 펼치고 이벤트를 선택하여 플로우를 시작하도록 트리거 이벤트를 선택하십시오. 
1.  아직 애플리케이션에 연결되지 않은 경우 **_애플리케이션_에 연결**을 클릭하고 애플리케이션에 대한 로그인 세부사항을 입력하십시오.
    일부 애플리케이션에 대한 추가 연결 세부사항을 제공해야 할 수 있습니다. 특정 애플리케이션에 대한 인증 정보를 찾는 데 도움이 필요한 경우 [앱 사용 방법 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://developer.ibm.com/integration/docs/app-connect/how-to-guides-for-apps/)을 참조하십시오.
1.  애플리케이션을 펼치고 조치를 선택하여 두 번째 애플리케이션에서 트리거할 조치를 선택하십시오.
    필요한 경우 **애플리케이션에 연결**을 클릭하고 대상 애플리케이션에 대한 로그인 세부사항을 입력하십시오. 
1. 애플리케이션 간에 전송할 데이터를 입력하십시오.
    필드를 클릭한 후 맵핑 아이콘 ![맵핑 아이콘](/images/MappingIcon.jpg)을 클릭하여 소스 필드 이름을 수동으로 추가할 수 있습니다. 또한 텍스트를 입력하거나 변환 기능을 사용하여 소스 값을 사용자 정의할 수 있습니다. 자세한 정보는 [변환 사용 방법 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://developer.ibm.com/integration/docs/app-connect/faq/#faq_transforms)을 참조하십시오.
1. 선택사항: 다음을 수행하여 플로우 작동 방식을 세분화할 수 있습니다. 
    * 플로우에서 더하기 아이콘 ![애플리케이션 추가 아이콘](/images/AddApp.jpg)을 클릭하여 더 많은 대상 애플리케이션 및 조치를 추가하십시오. 
    * 특정 기준과 일치하는 항목을 검색하기 위해 검색 조치를 플로우에 추가하거나, 지정된 레코드의 수를 검색하거나, 오류 처리를 정의하거나, 검색된 항목을 처리하는 방법을 정의하십시오([App Connect를 사용하여 애플리케이션에서 항목 검색 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/using-ibm-app-connect-retrieve-items-applications/) 참조).
    * 플로우의 애플리케이션에서 수신된 데이터에 따라 다른 조치를 수행하도록 일부 조건부 로직을 추가하십시오([플로우에 조건부 로직 추가 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/adding-conditional-logic-flow/) 참조).

1. 플로우를 구성한 경우 제목 표시줄의 옵션 메뉴를 열고 **플로우 시작**를 클릭하십시오.

{{site.data.keyword.appconserviceshort}} 대시보드로 돌아가는 경우 실행 중인 플로우를 볼 수 있습니다. 이벤트가 첫 번째 애플리케이션에서 발생하는 경우 조치는 두 번째 애플리케이션에서 {{site.data.keyword.appconserviceshort}}를 통해 자동으로 트리거됩니다. {{site.data.keyword.appconserviceshort}} 대시보드에서 플로우의 상태를 볼 수 있습니다. 플로우의 로그를 보려면 햄버거 메뉴 ![햄버거 메뉴 아이콘](/images/HamburgerMenuSm.jpg)을 열고 **관리**를 펼친 후 **로그**를 클릭하십시오.

일부 예제를 포함한 이벤트 중심 플로우 작성에 대한 자세한 정보는 [이벤트 중심 플로우 작성 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/creating-event-driven-flow/)을 참조하십시오.

## API용 플로우 작성

개발자가 클라우드 기반 애플리케이션에서 데이터를 활용하는 애플리케이션을 작성할 수 있으려면 API를 제공할 수 있습니다. API용 플로우를 작성하려면 다음 단계를 완료하십시오. 
1. {{site.data.keyword.appconserviceshort}} 대시보드에서 **새로 작성** > **API용 플로우**를 클릭하십시오. 
1. API의 이름을 입력하십시오. 
1. API가 작동할 오브젝트 유형을 반영하는 모델의 이름을 입력한 후 **모델 작성**을 클릭하십시오.
1. API가 작동할 오브젝트의 구조를 정의하는 데 필요한 특성을 추가하십시오.
    예를 들어, API가 고객을 작성하거나 검색하는 경우 Customer_ID, First_Name, Last_Name 및 Email_Address라는 특성을 추가할 수 있습니다. 특성의 이름을 입력하거나 **애플리케이션에서 특성 선택**을 클릭하여 사용자가 연결된 하나 이상의 애플리케이션에서 특성을 추가할 수 있습니다. 
1. **오퍼레이션**을 클릭하여 API가 오브젝트와 상호작용하는 방법을 정의하고 필요한 오퍼레이션을 추가하십시오.  
1. 각 오퍼레이션의 경우 **플로우 구현**을 클릭하여 각 오퍼레이션이 작동하는 방법을 정의하는 플로우를 작성하십시오.  
1. 요청 및 응답 간에 하나 이상의 대상 애플리케이션을 플로우에 추가하십시오.
    플로우에서 다른 조건에 맞는 다른 사항을 수행하려는 일부 조건부 로직을 추가할 수도 있습니다([플로우에 조건부 로직 추가 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/adding-conditional-logic-flow/) 추가).
1. 플로우에서 **응답**을 클릭하여 오퍼레이션이 실행될 때 리턴될 응답을 정의하십시오. 대상 애플리케이션에서 사용 가능한 필드를 맵핑하십시오.  
1. **완료**를 클릭하여 모델로 돌아가십시오.
1. 모든 모델 및 오퍼레이션을 정의한 경우 메뉴에서 **API 시작**을 선택하여 API를 시작하십시오. 

API용 플로우를 작성했습니다. {{site.data.keyword.appconserviceshort}} 대시보드에서 API용 플로우가 API 아이콘으로 식별됩니다. 다른 플로우와 동일한 방식으로 API용 플로우를 시작하고 중지할 수 있습니다. API가 실행 중인 동안 API를 열 수 있으나 편집하려면 중지해야 합니다. 

예제를 포함한 API용 플로우 작성 방법에 대한 자세한 정보는 [API용 플로우 작성 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/creating-flows-api/)을 참조하십시오.

API 테스트 방법을 알아보려면 [API Connect를 통해 App Connect 플로우 노출 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://developer.ibm.com/integration/blog/2017/08/29/exposing-app-connect-flow-api-connect/)을 참조하십시오.


## IBM Integration Bus 통합 솔루션 실행(Enterprise 베타)

IBM Integration Bus 또는 App Connect Enterprise에서 개발한 통합 솔루션을 클라우드에 배치할 경우, IT 인프라를 확보하고 유지보수할 필요 없이 통합 솔루션을 구성하는 모든 아티팩트가 포함된 BAR 파일을 가져온 후 App Connect의 통합 서버에 컨텐츠를 실행할 수 있습니다. BAR 파일을 App Connect에 업로드하려면 IBM Integration Bus 버전 10.0.0.4 이상 또는 App Connect Enterprise가 직접 설치되어야 합니다.

App Connect에서 Integration Bus 또는 App Connect Enterprise 솔루션을 실행하려면 다음 단계를 완료하십시오.
1. {{site.data.keyword.appconserviceshort}} 대시보드에서 **새로 작성** > **BAR 파일 가져오기**를 클릭하십시오. 
1. 가져올 BAR 파일을 선택하고 이름을 편집한 후(해당 경우) **가져오기**를 클릭하십시오.
    인증 오류가 표시되는 경우 BAR 파일이 올바른지 확인하십시오([App Connect에서 BAR 파일이 올바르게 설정될 수 있는 요소 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/what-makes-a-bar-file-valid-for-app-connect-app-connect-enterprise-beta) 참조).
    통합 서버가 작성되고 이를 표시하도록 타일이 대시보드에 추가됩니다. 통합 서버가 구성되고 시작될 준비가 되었을 때 상태는 "준비 중"에서 "중지됨"으로 변경됩니다.  
1. 타일을 클릭하여 통합 서버를 여십시오. 
1. 통합 서버를 구성하십시오. 
    * 통합 솔루션에 적합한 설명을 추가하거나 편집하십시오.
    * HTTPS 기본 인증을 구성하십시오([HTTPS 기본 인증 구성 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/configuring-https-basic-authentication-app-connect-enterprise-beta) 참조).
    * 온프레미스 시스템에 연결할 수 있도록 정책을 첨부하십시오([App Connect의 통합 서버와 온프레미스 시스템 간의 보안 연결 구성 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/configuring-secure-connectivity-between-integration-servers-on-app-connect-and-on-premises-systems-app-connect-enterprise-beta) 참조).
1. 선택사항: 온프레미스 환경과 App Connect 간의 메시지 플로우 처리를 구분하려면 햄버거 메뉴 ![햄버거 메뉴 아이콘](/images/HamburgerMenuSm.jpg)를 열고 **관리**를 펼치고 **호출 가능한 플로우**를 선택하여 호출 가능한 플로우를 구성하십시오([App Connect와 Integration Bus 간의 메시지 플로우 처리 공유 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/sharing-message-flow-processing-between-app-connect-and-integration-bus-app-connect-enterprise-beta) 참조).
1. 구성을 완료한 경우 App Connect 대시보드로 돌아간 후 타일 메뉴를 열고 **시작**을 클릭하여 통합 서버를 시작하십시오. 

통합 서버가 실행 중인 경우 통합 서버를 열고 **로그 다운로드** 또는 **로그 보기**를 클릭하여 로그를 보고 다운로드할 수 있습니다. 로그를 보려면 로깅 정책을 통합 서버에 첨부해야 합니다([통합 서버용 로그 보기 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/viewing-logs-for-your-integration-servers-in-app-connect-enterprise-beta) 참조).

자세한 정보는 [App Connect에서 Integration Bus 솔루션 실행 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan)을 참조하십시오.
