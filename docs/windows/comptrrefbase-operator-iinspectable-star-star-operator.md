---
title: "ComPtrRefBase::operator IInspectable** 연산자 | Microsoft Docs"
ms.custom: ""
ms.date: "12/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "reference"
f1_keywords: 
  - "client/Microsoft::WRL::Details::ComPtrRefBase::operator IInspectable**"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "operator IInspectable** 연산자"
ms.assetid: 06ac1051-606c-449b-a566-cac78ca53762
caps.latest.revision: 5
caps.handback.revision: 5
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
---
# ComPtrRefBase::operator IInspectable** 연산자
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

WRL 인프라를 지원하며 사용자 코드에서 직접 사용할 수 없습니다.  
  
## 구문  
  
```  
operator IInspectable**() const;  
```  
  
## 설명  
 현재 [ptr\_](../windows/comptrrefbase-ptr-data-member.md) 데이터 멤버는 포인터에 \-포인터\-IInspectable 인터페이스를 캐스팅합니다.  
  
 현재 ComPtrRefBase IInspectable에서 파생 되지 않으면 오류가 생성 됩니다.  
  
 만일 **\_\_WRL\_CLASSIC\_COM\_\_** 정의되었을 경우, 이 캐스트는 사용가능합니다.  
  
## 요구 사항  
 **헤더:** client.h  
  
 **네임스페이스**Microsoft::WRL::Details  
  
## 참고 항목  
 [ComPtrRefBase 클래스](../windows/comptrrefbase-class.md)   
 [Microsoft::WRL::Details 네임스페이스](../windows/microsoft-wrl-details-namespace.md)