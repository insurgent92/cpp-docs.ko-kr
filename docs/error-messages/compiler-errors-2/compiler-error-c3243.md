---
title: "컴파일러 오류 C3243 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C3243
dev_langs:
- C++
helpviewer_keywords:
- C3243
ms.assetid: 35d8ad1a-377d-47df-be9d-c55eea23340f
caps.latest.revision: 6
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
ms.openlocfilehash: bbd6363499e2c0eec0365b8e445b7d3a0f7e05f2
ms.contentlocale: ko-kr
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-error-c3243"></a>컴파일러 오류 C3243
오버로드 함수가 'interface'에 의해 하나도 정의되지 않았습니다.  
  
 하려고 [명시적으로 재정의](../../cpp/explicit-overrides-cpp.md) 지정된 된 인터페이스에 존재 하지 않는 멤버입니다.  
  
 다음 샘플에서는 C3243을 생성합니다.  
  
```  
// C3243.cpp  
#pragma warning(disable:4199)  
__interface IX14A {  
   void g();  
};  
  
__interface IX14B {  
   void f();  
   void f(int);  
};  
  
class CX14 : public IX14A, public IX14B {  
public:  
   void IX14A::g();  
   void IX14B::f();  
   void IX14B::f(int);  
};  
  
void CX14::IX14A::f()   // C3243 occurs here  
{  
}  
```