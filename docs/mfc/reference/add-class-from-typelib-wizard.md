---
title: "Typelib에서 클래스 추가 마법사 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vc.codewiz.class.typelib"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "TypeLib의 클래스 추가 마법사[C++]"
  - "COM 인터페이스, 클래스 추가"
ms.assetid: 96152afd-9374-4649-a6ab-b0fa2a5592a3
caps.latest.revision: 10
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 10
---
# Typelib에서 클래스 추가 마법사
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

이 마법사에서는 사용 가능한 형식 라이브러리의 MFC 클래스를 추가합니다.  마법사에서는 선택된 형식 라이브러리에서 추가한 각 인터페이스에 대해 클래스를 만듭니다.  
  
 **추가할 클래스 위치**  
 클래스가 만들어지는 형식 라이브러리의 위치를 나타냅니다.  
  
|옵션|설명|  
|--------|--------|  
|**레지스트리**|형식 라이브러리가 시스템에 등록됩니다.  등록된 형식 라이브러리는 **사용 가능한 형식 라이브러리**에 표시됩니다.|  
|**파일**|형식 라이브러리가 반드시 시스템에 등록되지는 않지만 파일에는 포함됩니다.  **위치**에 파일 위치를 지정해야 합니다.|  
  
 **사용 가능한 형식 라이브러리**  
 현재 시스템에 등록되어 있는 형식 라이브러리를 표시합니다.  이 목록에서 형식 라이브러리를 선택하여 **인터페이스** 목록에 해당 인터페이스를 표시합니다.  
  
 형식 라이브러리 등록에 대한 자세한 내용은 MSDN Library의 “Inside Distributed COM: Type Libraries and Language Integration”을 참조하십시오.  
  
 **위치**  
 형식 라이브러리의 위치를 지정합니다.  **추가할 클래스 위치**에서 **파일**을 클릭하면 형식 라이브러리가 포함된 파일의 위치를 지정할 수 있습니다.  파일의 위치를 찾아 보려면 줄임표\(...\) 단추를 클릭합니다.  
  
 **인터페이스**  
 **사용 가능한 형식 라이브러리** 목록에서 현재 선택한 형식 라이브러리의 인터페이스를 표시합니다.  
  
|전송 단추|설명|  
|-----------|--------|  
|**\>**|**인터페이스** 목록에서 현재 선택된 인터페이스를 추가합니다.  인터페이스가 선택되지 않으면 희미하게 나타납니다.|  
|**\>\>**|**사용 가능한 형식 라이브러리** 목록에서 현재 선택한 형식 라이브러리의 모든 인터페이스를 추가합니다.|  
|**\<**|**생성된 클래스** 목록에서 현재 선택된 클래스를 제거합니다.  **생성된 클래스** 목록에서 현재 선택된 클래스가 없으면 이 옵션이 희미하게 나타납니다.|  
|**\<\<**|**생성된 클래스** 목록의 클래스를 모두 제거합니다.  **생성된 클래스** 목록이 비어 있으면 이 옵션이 희미하게 나타납니다.|  
  
 **생성된 클래스**  
 Specifies the class names to be generated from the interfaces added using the **\>** or **\>\>** button.  이 상자를 클릭하여 클래스를 선택한 다음 위 또는 아래 키를 사용하여 목록을 스크롤하여 **마침**을 클릭할 때 마법사에서 생성하는 **파일** 상자의 파일 이름과 `Class` 상자의 클래스 이름을 확인할 수 있습니다.  이 상자에서는 한 번에 하나의 클래스만 선택할 수 있습니다.  
  
 You can remove a class by selecting it in this list and clicking **\<**.  You do not need to select a class in the Generated classes box to remove all classes; by clicking **\<\<**, you remove all classes in the **Generated classes** box.  
  
 `Class`  
 **마침**을 클릭할 때 마법사에서 추가하는 **생성된 클래스** 상자의 선택된 클래스 이름을 지정합니다.  `Class` 상자에서는 이름을 편집할 수 있습니다.  
  
 **파일**  
 새 클래스의 헤더 파일 이름을 설정합니다.  기본적으로 이 이름은 **생성된 클래스**에 입력한 이름을 기본으로 합니다.  원하는 위치에 파일 이름을 저장하거나 기존 파일에 클래스 선언을 추가하려면 줄임표\(...\) 단추를 클릭합니다.  기존 파일을 선택하면 마법사에서 **마침**을 클릭할 때까지 선택한 위치에 파일이 저장되지 않습니다.  
  
 또한 마법사에서는 파일을 덮어쓰지 않습니다.  기존 파일 이름을 선택한 경우 **마침**을 클릭하면 파일 내용에 클래스 선언을 추가할 것인지 묻는 메시지가 나타납니다.  파일을 추가하려면 **예**를 클릭하고, 마법사로 돌아가서 다른 파일 이름을 지정하려면 **아니요**를 클릭합니다.  
  
## 참고 항목  
 [형식 라이브러리의 MFC 클래스](../../mfc/reference/adding-an-mfc-class-from-a-type-library.md)   
 [자동화 클라이언트: 형식 라이브러리 사용](../../mfc/automation-clients-using-type-libraries.md)