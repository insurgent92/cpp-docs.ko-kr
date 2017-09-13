---
title: "컴파일러 오류 C3851 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C3851"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C3851"
ms.assetid: da30c21c-33aa-4439-8fb3-2f5021ea4985
caps.latest.revision: 7
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 7
---
# 컴파일러 오류 C3851
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'char': 유니버설 문자 이름에는 기본 문자 집합의 문자를 지정할 수 없습니다.  
  
 C\+\+로 컴파일된 코드에서는 문자열 또는 문자 리터럴 외부에서 기본 소스 문자 집합의 문자를 나타내는 유니버설 문자 이름을 사용할 수 없습니다. 자세한 내용은 [문자 집합](../../cpp/character-sets2.md)을 참조하세요. C로 컴파일된 코드에서는 0x24\('$'\), 0x40\('@'\) 또는 0x60\('\`'\)을 제외하고 0x20\-0x7f\(포함\) 범위의 문자에 유니버설 문자 이름을 사용할 수 없습니다.  
  
 다음 샘플에서는 C3851을 생성하고 해결 방법을 보여 줍니다.  
  
```cpp  
// C3851.cpp int main() { int test1_\u0041 = 0;   // C3851, \u0041 = 'A' in basic character set int test2_A = 0;        // OK }  
```