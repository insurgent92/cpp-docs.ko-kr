---
title: "컴파일러 경고 (수준 1) C4319 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C4319"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C4319"
ms.assetid: 1fac8048-9bd6-4552-a21c-192c67772bb9
caps.latest.revision: 7
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 7
---
# 컴파일러 경고 (수준 1) C4319
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'operator': 'type'을\(를\) 더 큰 'type'\(으\)로 0 확장합니다.  
  
 ~\(비트 보수\) 연산자의 결과에 부호가 없으면 더 큰 형식으로 변환될 때 0 확장됩니다.  
  
 다음 예제에서는 ~\(a \- 1\)이 32비트 부호 없는 long 식으로 계산된 다음 0 확장을 통해 64비트로 변환됩니다.  따라서 예기치 않은 결과가 발생할 수 있습니다.  
  
```  
// C4319.cpp  
// compile with: cl /W4 C4319.cpp  
int main() {  
   unsigned long a = 0;  
   unsigned long long q = 42;  
   q = q & ~(a - 1);    // C4319 expected  
}  
```