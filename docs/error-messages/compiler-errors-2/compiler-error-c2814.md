---
title: "컴파일러 오류 C2814 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2814
dev_langs:
- C++
helpviewer_keywords:
- C2814
ms.assetid: 7d165136-a08b-4497-a76d-60a21bb19404
caps.latest.revision: 16
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.ht:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
ms.translationtype: Machine Translation
ms.sourcegitcommit: c243063a9770542f137d5950e8a269f771960f74
ms.openlocfilehash: 164ad4f3862008a2352fc235df09b17e99cbfe83
ms.contentlocale: ko-kr
ms.lasthandoff: 02/24/2017

---
# <a name="compiler-error-c2814"></a>컴파일러 오류 C2814
'member' : 네이티브 형식은 관리되는 형식 또는 WinRT 형식 'type' 내부에 중첩될 수 없습니다.  
  
## <a name="example"></a>예제  
 네이티브 형식은 CLR 또는 WinRT 형식에 중첩할 수 없습니다. 다음 샘플에서는 C2814 오류가 발생하는 경우 및 이를 해결하는 방법을 보여 줍니다.  
  
```  
// C2814.cpp  
// compile with: /clr /c  
ref class A {  
   class B {};   // C2814  
   ref class C {};   // OK  
};  
```  
