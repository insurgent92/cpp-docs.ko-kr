---
title: "컴파일러 오류 C3228 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C3228
dev_langs:
- C++
helpviewer_keywords:
- C3228
ms.assetid: 9015adf9-17b0-4312-b4a7-c1f33e4126f4
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
ms.openlocfilehash: f1607de1e5ad0335cdf337a7418efa8eafa12823
ms.contentlocale: ko-kr
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-error-c3228"></a>컴파일러 오류 C3228
'function': 'param'에 대한 제네릭 형식 인수는 'type'일 수 없으며 값 형식이거나 핸들 형식이어야 합니다.  
  
 잘못된 형식이 제네릭 형식 인수로 전달되었습니다.  
  
 다음 샘플에서는 C3228을 생성합니다.  
  
```  
// C3228.cpp  
// compile with: /clr  
class A {};  
  
value class B {};  
  
generic <class T>  
void Test() {}  
  
ref class C {  
public:  
   generic <class T>  
   static void f() {}  
};  
  
int main() {  
   C::f<A>();   // C3228  
   C::f<B>();   // OK  
  
   Test<C>();   // C3228  
   Test<C ^>();   // OK  
}  
```