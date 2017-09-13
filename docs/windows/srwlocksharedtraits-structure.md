---
title: "SRWLockSharedTraits 구조체 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "reference"
f1_keywords: 
  - "corewrappers/Microsoft::WRL::Wrappers::HandleTraits::SRWLockSharedTraits"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "SRWLockSharedTraits 구조체"
ms.assetid: 709cb51e-d70c-40b6-bdb4-d8eacf3af495
caps.latest.revision: 3
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 3
---
# SRWLockSharedTraits 구조체
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

공유 잠금 모드에서 SRWLock 클래스의 공통적인 특성을 설명합니다.  
  
## 구문  
  
```  
struct SRWLockSharedTraits;  
```  
  
## 멤버  
  
### 공용 Typedefs  
  
|Name|설명|  
|----------|--------|  
|`Type`|[SRWLOCK](../windows/srwlock-class.md) 클래스에 대한 포인터 동의어입니다.|  
  
### Public 메서드  
  
|Name|설명|  
|----------|--------|  
|[SRWLockSharedTraits::GetInvalidValue 메서드](../windows/srwlocksharedtraits-getinvalidvalue-method.md)|항상 유효 하지 않은 SRWLockSharedTraits 개체를 검색 합니다.|  
|[SRWLockSharedTraits::Unlock 메서드](../windows/srwlocksharedtraits-unlock-method.md)|지정된 SRWLock 개체의 단독 제어를 해제합니다.|  
  
## 상속 계층  
 `SRWLockSharedTraits`  
  
## 요구 사항  
 **헤더:** corewrappers.h  
  
 **네임스페이스**Microsoft::WRL::Wrappers::HandleTraits  
  
## 참고 항목  
 [Microsoft::WRL::Wrappers::HandleTraits 네임스페이스](../windows/microsoft-wrl-wrappers-handletraits-namespace.md)