---
title: "저장 프로시저 사용 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "OLE DB 공급자 템플릿, 저장 프로시저"
  - "OLE DB, 저장 프로시저"
  - "저장 프로시저, 저장 프로시저 정보"
  - "저장 프로시저, OLE DB"
  - "저장 프로시저, Visual C++"
ms.assetid: 90507e4c-eca2-46c9-ad8c-07e10dc1d41b
caps.latest.revision: 16
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 16
---
# 저장 프로시저 사용
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

저장 프로시저는 데이터베이스에 저장된 실행 가능한 개체입니다.  저장 프로시저를 호출하는 것은 SQL 명령을 호출하는 것과 비슷합니다.  클라이언트 응용 프로그램에서 문을 실행하거나 준비하는 대신 데이터 소스에서 저장 프로시저를 사용하면, 성능 향상, 네트워크 오버헤드 감소, 일관성 및 정확성 개선 등의 여러 가지 장점이 있습니다.  
  
 저장 프로시저는 원하는 만큼의 입력이나 출력 매개 변수를 가질 수 있으며\(매개 변수가 없을 수도 있음\) 반환 값을 전달할 수 있습니다.  사용자는 매개 변수 값을 특정 데이터 값으로 하드 코딩하거나 매개 변수 마커\(물음표 '?'\)를 사용할 수도 있습니다.  
  
> [!NOTE]
>  Visual C\+\+를 사용하여 만든 CLR SQL Server 저장 프로시저는 **\/clr:safe** 컴파일러 옵션을 사용하여 컴파일해야 합니다.  
  
 SQL Server용 OLE DB 공급자\(SQLOLEDB\)는 데이터를 반환하기 위해 저장 프로시저가 사용하는 다음 메커니즘을 지원합니다.  
  
-   프로시저의 모든 SELECT 문은 결과 집합을 생성합니다.  
  
-   프로시저는 출력 매개 변수를 통해 데이터를 반환할 수 있습니다.  
  
-   프로시저에는 정수 반환 코드가 있을 수 있습니다.  
  
> [!NOTE]
>  Jet용 OLE DB 공급자는 저장 프로시저를 지원하지 않으므로 Jet용 OLE DB 공급자로 저장 프로시저를 사용할 수 없습니다. 쿼리 문자열에는 상수만 사용할 수 있습니다.  
  
## 참고 항목  
 [OLE DB 소비자 템플릿 작업](../../data/oledb/working-with-ole-db-consumer-templates.md)