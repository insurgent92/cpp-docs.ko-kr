---
title: "C++ 연산자, 우선 순위 및 결합성 | Microsoft Docs"
ms.custom: ""
ms.date: "12/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "language-reference"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "연산자 결합성"
  - "평가 순서"
  - "계층 구조, operator"
  - "다중 연산자"
  - "연산자 우선 순위"
  - "연산자[C++], 결합성"
  - "연산자[C++], 계층 구조"
  - "연산자[C++], 우선 순위"
  - "우선 순위, 연산자"
ms.assetid: 95c1f0ba-dad8-4034-b039-f79a904f112f
caps.latest.revision: 13
caps.handback.revision: 13
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
---
# C++ 연산자, 우선 순위 및 결합성
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

C\+\+ 언어는 모든 C 연산자를 포함하며 몇 가지 새로운 연산자를 추가합니다.  연산자는 둘 이상의 피연산자에 대해 수행할 평가를 지정합니다.  
  
 연산자 우선 순위는 둘 이상의 연산자를 포함하는 식에서 연산의 순서를 지정합니다.  연산자 결합성은 우선 순위가 같은 여러 연산자를 포함하는 식에서 피연산자가 왼쪽의 연산자 또는 오른쪽의 연산자와 그룹화되는지 지정합니다.  다음 표에서는 C\+\+ 연산자의 우선 순위와 결합성을 내림차순으로 보여 줍니다.  우선 순위 번호가 같은 연산자는 괄호를 사용하여 다른 관계를 명시적으로 강제하지 않는 한 우선 순위가 같습니다.  
  
### C\+\+ 연산자 우선 순위 및 결합성  
  
|연산자 설명|연산자|  
|------------|---------|  
|`Group 1 precedence, no associativity`|  
|[범위 확인](../cpp/scope-resolution-operator.md)|`::`|  
|`Group 2 precedence, left to right associativity`|  
|[멤버 선택\(개체 또는 포인터\)](../cpp/member-access-operators-dot-and.md)|`. or –>`|  
|[배열 첨자](../cpp/subscript-operator.md)|`[ ]`|  
|[함수 호출](../cpp/function-call-operator-parens.md)|`( )`|  
|[후위 증가](../cpp/postfix-increment-and-decrement-operators-increment-and-decrement.md)|`++`|  
|[후위 감소](../cpp/postfix-increment-and-decrement-operators-increment-and-decrement.md)|`––`|  
|[형식 이름](../cpp/typeid-operator.md)|`typeid( )`|  
|[상수 형식 변환](../cpp/const-cast-operator.md)|`const_cast`|  
|[동적 형식 변환](../cpp/dynamic-cast-operator.md)|`dynamic_cast`|  
|[재해석 형식 변환](../cpp/reinterpret-cast-operator.md)|`reinterpret_cast`|  
|[정적 형식 변환](../cpp/static-cast-operator.md)|`static_cast`|  
|`Group 3 precedence, right to left associativity`|  
|[개체 또는 형식의 크기](../cpp/sizeof-operator.md)|`sizeof`|  
|[전위 증가](../cpp/prefix-increment-and-decrement-operators-increment-and-decrement.md)|`++`|  
|[전위 감소](../cpp/prefix-increment-and-decrement-operators-increment-and-decrement.md)|`––`|  
|[1의 보수](../cpp/one-s-complement-operator-tilde.md)|`~`|  
|[논리 NOT](../cpp/logical-negation-operator-exclpt.md)|`!`|  
|[단항 부정 연산자](../misc/unary-negation-operator.md)|`-`|  
|[단항 더하기](../cpp/unary-plus-and-negation-operators-plus-and.md)|`+`|  
|[Address\-of](../cpp/lvalue-reference-declarator-amp.md)|`&`|  
|[간접 참조](../cpp/indirection-operator-star.md)|`*`|  
|[개체 만들기](../cpp/new-operator-cpp.md)|`new`|  
|[개체 삭제](../cpp/delete-operator-cpp.md)|`delete`|  
|[Cast](../cpp/cast-operator-parens.md)|`Cast: ()`|  
|`Group 4 precedence, left to right associativity`|  
|[멤버 포인터\(개체 또는 포인터\)](../cpp/pointer-to-member-operators-dot-star-and-star.md)|`.* or –>*`|  
|`Group 5 precedence, left to right associativity`|  
|[곱하기](../cpp/multiplicative-operators-and-the-modulus-operator.md)|`*`|  
|[나누기](../cpp/multiplicative-operators-and-the-modulus-operator.md)|`/`|  
|[모듈러스](../cpp/multiplicative-operators-and-the-modulus-operator.md)|`%`|  
|`Group 6 precedence, left to right associativity`|  
|[더하기](../cpp/additive-operators-plus-and.md)|`+`|  
|[빼기](../cpp/additive-operators-plus-and.md)|`–`|  
|`Group 7 precedence, left to right associativity`|  
|[왼쪽 시프트](../cpp/left-shift-and-right-shift-operators-input-and-output.md)|`<<`|  
|[오른쪽 시프트](../cpp/left-shift-and-right-shift-operators-input-and-output.md)|`>>`|  
|`Group 8 precedence, left to right associativity`|  
|[보다 작음](../cpp/relational-operators-equal-and-equal.md)|`<`|  
|[보다 큼](../cpp/relational-operators-equal-and-equal.md)|`>`|  
|[작거나 같음](../cpp/relational-operators-equal-and-equal.md)|`<=`|  
|[크거나 같음](../cpp/relational-operators-equal-and-equal.md)|`>=`|  
|`Group 9 precedence, left to right associativity`|  
|[같음](../cpp/equality-operators-equal-equal-and-exclpt-equal.md)|`==`|  
|[같지 않음](../cpp/equality-operators-equal-equal-and-exclpt-equal.md)|`!=`|  
|`Group 10 precedence left to right associativity`|  
|[비트 AND](../cpp/bitwise-and-operator-amp.md)|`&`|  
|`Group 11 precedence, left to right associativity`|  
|[배타적 비트 OR](../cpp/bitwise-exclusive-or-operator-hat.md)|`^`|  
|`Group 12 precedence, left to right associativity`|  
|[포괄적 비트 OR](../cpp/bitwise-inclusive-or-operator-pipe.md)|`&#124;`|  
|`Group 13 precedence, left to right associativity`|  
|[논리 AND](../cpp/logical-and-operator-amp-amp.md)|`&&`|  
|`Group 14 precedence, left to right associativity`|  
|[논리곱 OR](../cpp/logical-or-operator-pipe-pipe.md)|`&#124;&#124;`|  
|`Group 15 precedence, right to left associativity`|  
|[조건](../cpp/conditional-operator-q.md)|`? :`|  
|`Group 16 precedence, right to left associativity`|  
|[할당](../cpp/assignment-operators.md)|`=`|  
|[곱하기 할당](../cpp/assignment-operators.md)|`*=`|  
|[나누기 할당](../cpp/assignment-operators.md)|`/=`|  
|[모듈러스 대입](../cpp/assignment-operators.md)|`%=`|  
|[더하기 할당](../cpp/assignment-operators.md)|`+=`|  
|[빼기 할당](../cpp/assignment-operators.md)|`–=`|  
|[왼쪽 시프트 할당](../cpp/assignment-operators.md)|`<<=`|  
|[오른쪽 시프트 할당](../cpp/assignment-operators.md)|`>>=`|  
|[비트 AND 대입](../cpp/assignment-operators.md)|`&=`|  
|[포괄적 비트 OR 대입](../cpp/assignment-operators.md)|`&#124;=`|  
|[배타적 비트 OR 대입](../cpp/assignment-operators.md)|`^=`|  
|`Group 17 precedence, right to left associativity`|  
|[throw 식](../cpp/try-throw-and-catch-statements-cpp.md)|`throw`|  
|`Group 18 precedence, left to right associativity`|  
|[쉼표](../cpp/comma-operator.md)|`,`|  
  
## 참고 항목  
 [C\+\+ 연산자](../misc/cpp-operators.md)   
 [연산자 오버로드](../cpp/operator-overloading.md)