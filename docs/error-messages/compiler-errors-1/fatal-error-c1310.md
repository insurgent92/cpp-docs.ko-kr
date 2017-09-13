---
title: "심각한 오류 C1310 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C1310
dev_langs:
- C++
helpviewer_keywords:
- C1310
ms.assetid: ac48aa51-8023-42fe-b844-3f8bf228fbef
caps.latest.revision: 5
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.ht:
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- ru-ru
- zh-cn
- zh-tw
translation.priority.mt:
- cs-cz
- pl-pl
- pt-br
- tr-tr
ms.translationtype: Machine Translation
ms.sourcegitcommit: 0d9cbb01d1ad0f2ea65d59334cb88140ef18fce0
ms.openlocfilehash: 1cba1d5ea85b4eb97fb1b1b9091b1710a2a59490
ms.contentlocale: ko-kr
ms.lasthandoff: 04/12/2017

---
# <a name="fatal-error-c1310"></a>심각한 오류 C1310
OpenMP에서는 프로필 기반 최적화를 사용할 수 없습니다.  
  
 와 연결할 수 없습니다 [/ltcg: pgi](../../build/reference/ltcg-link-time-code-generation.md) 으로 컴파일된 모든 모듈 [/GL](../../build/reference/gl-whole-program-optimization.md)합니다.  
  
 다음 샘플에서는 C1310을 생성합니다.  
  
```  
// C1310.cpp  
// compile with: /openmp /GL /link /LTCG:PGI  
// C1310 expected  
int main()  
{  
   int i = 0, j = 10;  
  
   #pragma omp parallel  
   {  
      #pragma omp for  
      for (i = 0; i < 0; i++)   
         --j;  
   }  
}  
```