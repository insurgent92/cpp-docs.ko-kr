---
title: "컴파일러 오류 C3039 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C3039
dev_langs:
- C++
helpviewer_keywords:
- C3039
ms.assetid: 02776f16-f57a-4ffd-b7f7-9c696b633e08
caps.latest.revision: 8
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
ms.openlocfilehash: af2d6ef4fe93730265de6081fcb83f074dc6e4ec
ms.contentlocale: ko-kr
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-error-c3039"></a>컴파일러 오류 C3039
'var': OpenMP 'for' 문의 인덱스 변수는 환산(reduction) 변수가 될 수 없습니다.  
  
 변수에서 사용할 수 없도록 인덱스 변수는 암시적으로 비공개는 [감소](../../parallel/openmp/reference/reduction.md) 절의 바깥쪽 [병렬](../../parallel/openmp/reference/parallel.md) 지시문입니다.  
  
## <a name="example"></a>예제  
 다음 샘플에서는 C3039를 생성합니다.  
  
```  
// C3039.cpp  
// compile with: /openmp /c  
int g_i;  
  
int main() {  
   int i;  
  
   #pragma omp parallel reduction(+: i)  
   {  
      #pragma omp for  
      for (i = 0; i < 10; ++i)   // C3039  
         g_i += i;  
   }  
}  
```