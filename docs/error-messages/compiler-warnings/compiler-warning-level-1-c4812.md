---
title: "컴파일러 경고 (수준 1) C4812 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C4812
dev_langs:
- C++
helpviewer_keywords:
- C4812
ms.assetid: a7f5721f-2019-44de-ad62-ed30bac8b1f3
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
ms.openlocfilehash: a52ef0b5af82481fae720b940ddbd35b2793fd55
ms.contentlocale: ko-kr
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-warning-level-1-c4812"></a>컴파일러 경고(수준 1) C4812
사용되지 않는 선언 스타일입니다. 대신 'new_syntax'를 사용하세요.  
  
 현재 릴리스의 Visual C++에서는 명시적 생성자 특수화가 지원되지만 이후 릴리스에서는 지원되지 않을 수 있습니다.  
  
 다음 샘플에서는 C4812를 생성합니다.  
  
```  
// C4812.cpp  
// compile with: /W1 /c  
template <class T>   
class MyClass;  
  
template<class T>  
class MyClass<T*> {  
   MyClass();  
};  
  
template<class T>  
MyClass<T*>::MyClass<T*>() {}   // C4812  
// try the following line instead  
// MyClass<T*>::MyClass() {}  
```