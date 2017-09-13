---
title: "괄호를 사용한 식 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-language
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- C++
helpviewer_keywords:
- parentheses
- expression evaluation, evaluation order
- expressions [C++], evaluating
- parentheses, expressions
ms.assetid: b8636147-6982-408c-9e64-29e40678ee43
caps.latest.revision: 7
author: mikeblome
ms.author: mblome
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
ms.translationtype: Human Translation
ms.sourcegitcommit: d6eb43b2e77b11f4c85f6cf7e563fe743d2a7093
ms.openlocfilehash: 70a20f37096571259e2664472c6a2989daa4bd86
ms.contentlocale: ko-kr
ms.lasthandoff: 05/18/2017

---
# <a name="expressions-in-parentheses"></a>괄호를 사용한 식
괄호 안에 포함된 식의 형식이나 값을 변경하지 않고 임의의 피연산자를 괄호로 묶을 수 있습니다. 예를 들어 다음 식에서  
  
```  
( 10 + 5 ) / 5  
```  
  
 `10 + 5` 주위의 괄호는 `10 + 5` 값이 먼저 계산되어 나누기 연산자(**/**)의 왼쪽 피연산자가 된다는 의미입니다. `( 10 + 5 ) / 5`의 결과는 3입니다. 괄호가 없으면 `10 + 5 / 5`는 11로 계산됩니다.  
  
 괄호는 피연산자가 식에서 그룹화되는 방식에 영향을 주지만 모든 경우에 계산의 특정 순서를 보장할 수 있는 것은 아닙니다. 예를 들어 다음 식의 괄호와 왼쪽-오른쪽 그룹화는 하위 식 중 하나에서 사용될 `i`의 값을 보장하지 않습니다.  
  
```  
( i++ +1 ) * ( 2 + i )  
```  
  
 컴파일러는 순서에 상관없이 곱하기의 양쪽을 계산할 수 있습니다. `i`의 초기 값이 0인 경우 전체 식은 다음 두 문 중 하나로 계산될 수 있습니다.  
  
```  
( 0 + 1 + 1 ) * ( 2 + 1 )   
( 0 + 1 + 1 ) * ( 2 + 0 )  
```  
  
 의도하지 않은 결과로 발생한 예외는 [파생 작업](../c-language/side-effects.md)에 설명되어 있습니다.  
  
## <a name="see-also"></a>참고 항목  
 [C 기본 식](../c-language/c-primary-expressions.md)