---
title: "컨트롤 추가(ATL 자습서, 2부) | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "get-started-article"
dev_langs: 
  - "C++"
ms.assetid: c9575a75-1064-41f1-9697-7aada560c669
caps.latest.revision: 15
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 10
---
# 컨트롤 추가(ATL 자습서, 2부)
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

이 단계에서는 컨트롤을 프로젝트에 추가하고 빌드하며 웹 페이지에서 테스트합니다.  
  
## 절차  
  
#### ATL 프로젝트에 개체를 추가하려면  
  
1.  클래스 뷰에서 Polygon 프로젝트를 마우스 오른쪽 단추로 클릭합니다.  
  
2.  바로 가기 메뉴에서 **추가** 를 지정하여, 하위 메뉴의 **클래스** 를 클릭합니다.  
  
     **클래스 추가** 대화 상자가 나타납니다.  다른 개체 범주는 왼쪽의 트리 구조로 나열됩니다.  
  
3.  **ATL** 폴더를 클릭합니다.  
  
4.  오른쪽에 있는 템플릿 목록에서 **ATL 컨트롤**을 선택합니다.  **추가**를 클릭합니다.  ATL 컨트롤 마법사가 열리고 컨트롤을 구성할 수 있습니다.  
  
5.  다른 필드가 자동으로 완성되는 짧은 이름 및 메모의 `PolyCtl` 형식입니다.  아직 일부를 변경해야 하므로 **마침** 을 클릭하지 마십시오.  
  
 ATL 컨트롤 마법사의 **이름** 페이지에는 다음과 같은 필드가 포함되어 있습니다.  
  
|필드|내용|  
|--------|--------|  
|**약식 이름**|컨트롤을 위해 입력했던 이름입니다.|  
|**클래스**|C\+\+ 클래스 이름은 컨트롤을 구현하기 위해 생성됩니다.|  
|**.h 파일**|이 파일은 C\+\+ 클래스의 정의를 포함하기 위해 만들어집니다.|  
|**.cpp 파일**|이 파일은 C\+\+ 클래스의 구현을 포함하기 위해 만들어집니다.|  
|**CoClass**|이 컨트롤을 위한 구성 요소 클래스 이름입니다.|  
|**Interface**|컨트롤이 사용자 지정 메서드 및 속성을 구현할 인터페이스의 이름입니다.|  
|**형식**|컨트롤에 대한 설명입니다.|  
|**ProgID**|컨트롤의 CLSID를 찾는 데 사용할 수 있는 읽을 수 있는 이름입니다.|  
  
 ATL 컨트롤 마법사에서 일부 추가 설정을 수행해야 합니다.  
  
#### 다양한 오류 정보와 연결 지점에 대한 지원을 사용하려면  
  
1.  **옵션** 페이지를 열려면 **옵션** 을 클릭합니다.  
  
2.  **연결 지점** 확인란을 선택합니다.  그러면 IDL 파일에 송신 인터페이스에 대한 지원이 만들어집니다.  
  
 컨트롤을 삽입 가능하게 할 수 있습니다. 즉, 포함 개체를 지원하는 Excel 또는 Word와 같은 응용 프로그램에 포함될 수 있음을 의미합니다.  
  
#### 컨트롤을 삽입 가능하도록 설정하려면  
  
1.  **모양** 페이지를 열려면 **모양** 을 클릭합니다.  
  
2.  **삽입 가능** 확인란을 선택합니다.  
  
 개체별로 표시된 다각형에는 단색 채우기 색이 사용되므로 `Fill Color` 스톡 속성을 추가해야 합니다.  
  
#### 채우기 색 스톡 속성을 추가하고 컨트롤을 만들려면  
  
1.  **스톡 속성** 페이지를 열려면 **스톡 속성** 을 클릭합니다.  
  
2.  **지원되지 않음**에서 가능한 스톡 속성 목록을 아래로 스크롤합니다.  `Fill Color` 을 두 번 클릭하여 **지원됨** 목록으로 이동합니다.  
  
3.  그러면 컨트롤의 옵션이 완료됩니다.  **마침**을 클릭합니다.  
  
 마법사가 컨트롤을 만들었을 때 몇 가지 코드 변경 내용 및 파일 추가가 발생했습니다.  다음과 같은 파일이 생성되었습니다.  
  
|파일|설명|  
|--------|--------|  
|PolyCtl.h|대부분의 C\+\+ 클래스 `CPolyCtl`의 구현이 포함됩니다.|  
|PolyCtl.cpp|`CPolyCtl`의 나머지 부분이 포함됩니다.|  
|PolyCtl.rgs|컨트롤을 등록하는 데 사용하는 레지스트리 스크립트를 포함하는 텍스트 파일입니다.|  
|PolyCtl.htm|새로 만든 컨트롤에 대한 참조를 포함하는 웹 페이지입니다.|  
  
 마법사는 다음과 같이 코드 변경도 수행합니다.  
  
-   `#include` 문을 stdafx.h 및 stdafx.cpp 파일에 추가하여 제어를 지원하는 데 필요한 ATL 파일을 포함합니다.  
  
-   새 컨트롤의 세부 정보가 포함되도록 Polygon.idl을 변경했습니다.  
  
-   새 컨트롤이 Polygon.cpp의 개체 맵에 추가되었습니다.  
  
 이제 작업을 보기 위해 컨트롤을 빌드할 수 있습니다.  
  
## 컨트롤 빌드 및 테스트  
  
#### 컨트롤을 빌드하고 테스트하려면  
  
1.  **빌드** 메뉴에서 **다각형 빌드**를 클릭합니다.  
  
     컨트롤이 빌드를 완료하면, **솔루션 탐색기** 에서 PolyCtl.htm을 마우스 오른쪽 단추로 클릭하고, **브라우저에서 보기**를 선택합니다.  제어를 포함하는 HTML 웹페이지가 표시될 것 입니다.  "PolyCtl 개체에 대한 ATL 8.0 테스트 페이지"라는 제목 및 **PolyCtl**라는 텍스트를 가진 페이지가 나타납니다.  사용자의 컨트롤입니다.  
  
> [!NOTE]
>  이 자습서를 작성할 때 DLL 파일을 생성할 수 없다는 오류 메시지가 표시되는 경우 PolyCtl.htm 파일 및 Active X 컨트롤 테스트 컨테이너를 닫고 솔루션을 다시 빌드합니다.  DLL을 만들 수 엇는 경우 컴퓨터를 다시 부팅하거나 로그오프합니다\(터미널 서비스를 사용 중인 경우\).  
  
 다음으로 컨트롤에 사용자 지정 속성을 추가할 것 입니다.  
  
 [1단계로 돌아가기](../atl/creating-the-project-atl-tutorial-part-1.md) &#124; [3단계로 이동합니다.](../atl/adding-a-property-to-the-control-atl-tutorial-part-3.md)  
  
## 참고 항목  
 [자습서](../atl/active-template-library-atl-tutorial.md)