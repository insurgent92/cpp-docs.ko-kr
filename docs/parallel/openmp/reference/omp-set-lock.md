---
title: "omp_set_lock | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "omp_set_lock"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "omp_set_lock OpenMP function"
ms.assetid: ded839cb-ca19-403f-8622-eb52ce512d31
caps.latest.revision: 7
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 7
---
# omp_set_lock
[!INCLUDE[vs2017banner](../../../assembler/inline/includes/vs2017banner.md)]

잠금을 사용할 수 있을 때까지 실행 스레드를 차단.  
  
## 구문  
  
```  
void omp_set_lock(  
   omp_lock_t *lock  
);  
```  
  
## 설명  
 다음은 각 매개 변수에 대한 설명입니다.  
  
 `lock`  
 형식의 변수에 [omp\_lock\_t](../../../parallel/openmp/reference/omp-lock-t.md) 로 초기화 된 [omp\_init\_lock](../../../parallel/openmp/reference/omp-init-lock.md).  
  
## 설명  
 자세한 내용은 [3.2.3 omp\_set\_lock and omp\_set\_nest\_lock Functions](../../../parallel/openmp/3-2-3-omp-set-lock-and-omp-set-nest-lock-functions.md)를 참조하십시오.  
  
## 예제  
 참조 하십시오 [omp\_init\_lock](../../../parallel/openmp/reference/omp-init-lock.md) 를 사용 하는 예에 대 한 `omp_set_lock`.  
  
## 참고 항목  
 [Functions](../../../parallel/openmp/reference/openmp-functions.md)