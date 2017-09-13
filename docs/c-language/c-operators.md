---
title: "C 연산자 | Microsoft Docs"
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
- ternary operators
- operators [C]
- symbols, operators
- binary operators
- associativity of operators
- binary data, binary expressions
ms.assetid: 13bc4c8e-2dc9-4b23-9f3a-25064e8777ed
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
ms.sourcegitcommit: 3f91eafaf3b5d5c1b8f96b010206d699f666e224
ms.openlocfilehash: 6eab29bde1fe9b08e0883960ed7a160101d56d1a
ms.contentlocale: ko-kr
ms.lasthandoff: 04/01/2017

---
# <a name="c-operators"></a>C 연산자
C 연산자는 [C++ 기본 제공 연산자](../cpp/cpp-built-in-operators-precedence-and-associativity.md)의 하위 집합입니다.  
  
 연산자의 형식에는 다음 세 가지가 있습니다. 단항 식은 피연산자 앞에 추가된 단항 연산자 또는 식 뒤에 오는 `sizeof` 키워드로 구성됩니다. 식은 변수 이름이나 캐스트 식이 될 수 있습니다. 캐스트 식인 경우 괄호로 묶어야 합니다. 이항 식은 이항 연산자로 결합된 두 개의 피연산자로 구성됩니다. 삼진 식은 조건식 연산자로 결합된 세 개의 피연산자로 구성됩니다.  
  
 C에는 다음과 같은 단항 연산자가 포함되어 있습니다.  
  
|기호|이름|  
|------------|----------|  
|**- ~ !**|부정 및 보수 연산자|  
|**\* &**|간접 참조 및 주소 연산자|  
|`sizeof`|크기 연산자|  
|**+**|단항 더하기 연산자|  
|**++ --**|단항 증가 및 감소 연산자|  
  
 이항 연산자는 왼쪽에서 오른쪽으로 연결됩니다. C에서는 다음과 같은 이항 연산자를 제공합니다.  
  
|기호|이름|  
|------------|----------|  
|**\* / %**|곱하기 연산자|  
|**+ -**|더하기 연산자|  
|**<\< >>**|시프트 연산자|  
|**\<   >   \<=   >=   ==   !=**|관계형 연산자|  
|**&   &#124; ^**|비트 연산자|  
|**&&   &#124;&#124;**|논리 연산자|  
|**,**|순차적 계산 연산자|  
  
 Microsoft 16비트 C 컴파일러의 이전 버전에서 지원되는 기본 연산자(**:>**)는 [C 언어 구문 요약](../c-language/c-language-syntax-summary.md)에 설명되어 있습니다.  
  
 조건식 연산자는 이진 식보다 우선 순위가 낮으며 오른쪽 결합성에서 이진 식과 다릅니다.  
  
 또한 연산자가 있는 식은 단항 또는 이항 할당 연산자를 사용하는 할당 식을 포함합니다. 단항 대입 연산자는 증가(`++`) 및 감소(**--**) 연산자이며, 이항 대입 연산자는 단순 대입 연산자(**=**) 및 복합 대입 연산자입니다. 각 복합 할당 연산자는 이항 연산자와 단순 할당 연산자의 조합입니다.  
  
## <a name="see-also"></a>참고 항목  
 [식 및 할당](../c-language/expressions-and-assignments.md)