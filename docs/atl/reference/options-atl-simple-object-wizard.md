---
title: "옵션, ATL 단순 개체 마법사 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "reference"
f1_keywords: 
  - "vc.codewiz.class.atl.simple.options"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "ATL 단순 개체 마법사, 옵션"
ms.assetid: 125fe179-942d-4181-8b82-33e92e1fd779
caps.latest.revision: 14
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 14
---
# 옵션, ATL 단순 개체 마법사
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

ATL 단순 개체 마법사의 이 페이지에서는 효율성 및 오류 지원 능력이 향상된 개체를 디자인합니다.  
  
 ATL 프로젝트 및 ATL COM 클래스에 대한 자세한 내용은 [ATL COM Desktop Components](../../atl/atl-com-desktop-components.md)를 참조하십시오.  
  
 **스레딩 모델**  
 스레드를 관리하는 방법을 나타냅니다.  기본적으로 프로젝트에서는 **아파트** 스레딩을 사용합니다.  
  
 자세한 내용은 [프로젝트의 스레딩 모델 지정](../../atl/specifying-the-threading-model-for-a-project-atl.md)을 참조하십시오.  
  
|옵션|설명|  
|--------|--------|  
|`Single`|개체가 항상 기본 COM 스레드에서 실행되도록 지정합니다.  자세한 내용은 [Single\-Threaded Apartments](http://msdn.microsoft.com/library/windows/desktop/ms680112) 및 [InprocServer32](http://msdn.microsoft.com/library/windows/desktop/ms682390)를 참조하십시오.|  
|**아파트**|개체에서 아파트 스레딩을 사용하도록 지정합니다.  이 옵션은 단일 스레드 아파트와 동일합니다.  아파트 스레드된 구성 요소의 모든 개체에는 개체의 사용 기간 동안 해당 스레드에 대한 아파트가 할당되지만, 여러 개체에 여러 스레드를 사용할 수 있습니다.  모든 아파트는 특정 스레드에 연결되어 있으며 기본적으로 Windows 메시지 펌프를 갖습니다.<br /><br /> 자세한 내용은 [Single\-Threaded Apartments](http://msdn.microsoft.com/library/windows/desktop/ms680112)를 참조하십시오.|  
|**Both**|개체를 만들 때 사용한 스레드 종류에 따라 개체에서 아파트나 자유 스레딩을 사용할 수 있도록 지정합니다.|  
|**자유형**|개체에서 자유 스레딩을 사용하도록 지정합니다.  자유 스레딩은 다중 스레드 아파트 모델과 동일합니다.  자세한 내용은 [Multithreaded Apartments](http://msdn.microsoft.com/library/windows/desktop/ms693421)를 참조하십시오.|  
|**중립**\(Windows 2000 전용\)|개체가 다중 스레드 아파트의 지침을 따르지만 모든 종류의 스레드에서 실행될 수 있도록 지정합니다.|  
  
 **집계**  
 개체에서 [aggregation](http://msdn.microsoft.com/library/windows/desktop/ms686558)을 사용하는지 여부를 지정합니다.  집계 개체에서 클라이언트에 노출할 인터페이스를 선택하면 해당 인터페이스는 집계 개체에서 구현된 것처럼 노출됩니다.  집계 개체의 클라이언트는 집계 개체와만 통신합니다.  
  
|옵션|설명|  
|--------|--------|  
|예|개체가 집계될 수 있도록 지정합니다.  기본값입니다.|  
|아니요|개체가 집계되지 않도록 지정합니다.|  
|전용|개체가 반드시 집계되도록 지정합니다.|  
  
 **Interface**  
 개체에서 지원하는 인터페이스 형식을 나타냅니다.  기본적으로 개체에서는 이중 인터페이스를 지원합니다.  
  
|옵션|설명|  
|--------|--------|  
|**이중**|개체에서 이중 인터페이스를 지원하도록 지정합니다. 이 인터페이스의 vtable에는 사용자 지정 인터페이스 함수와 런타임 시 바인딩 `IDispatch` 메서드가 있습니다.  이중 인터페이스를 사용하면 COM 클라이언트와 [자동화 컨트롤러](../../mfc/automation-clients.md) 모두 개체에 액세스할 수 있습니다.  기본값입니다.|  
|**사용자 지정**|개체에서 사용자 지정 인터페이스를 지원하도록 지정합니다. 이 인터페이스의 vtable에는 사용자 지정 인터페이스 함수가 있습니다.  사용자 지정 인터페이스는 특히 프로세스 경계에서 이중 인터페이스보다 더 빠를 수 있습니다.<br /><br /> -   **자동화 호환** 수 있도록 자동화 컨트롤러에서 사용자 지정 인터페이스를 지 원하는 개체에 액세스할 수 있습니다.|  
  
 **지원**  
 개체에 대한 그 밖의 지원을 나타냅니다.  
  
|옵션|설명|  
|--------|--------|  
|**ISupportErrorInfo**|[ISupportErrorInfo](../../atl/reference/isupporterrorinfoimpl-class.md) 인터페이스에 대한 지원을 제공하여 개체에서 클라이언트로 오류 정보를 반환할 수 있도록 합니다.|  
|**연결 지점**|[IConnectionPointContainerImpl](../../atl/reference/iconnectionpointcontainerimpl-class.md)에서 개체 클래스를 파생시켜 개체의 연결 지점을 사용할 수 있도록 합니다.|  
|**자유 스레드된 마샬러**|같은 프로세스의 스레드 간에 인터페이스 포인터를 효율적으로 마샬링하도록 자유 스레드된 마샬러 개체를 만듭니다.  **모두**를 스레딩 모델로 지정하는 개체에 사용할 수 있습니다.|  
|**IObjectWithSite\(IE 개체 지원\)**|[IObjectWithSiteImpl](../../atl/reference/iobjectwithsiteimpl-class.md)을 구현하여 개체와 컨테이너의 해당 사이트 간에 통신을 지원하는 간단한 방법을 제공합니다.|  
  
## 참고 항목  
 [ATL 단순 개체 마법사](../../atl/reference/atl-simple-object-wizard.md)   
 [ATL Simple Object](../../atl/reference/adding-an-atl-simple-object.md)   
 [In\-Process 서버 스레딩 문제](http://msdn.microsoft.com/library/windows/desktop/ms687205)