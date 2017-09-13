---
title: "C 문자열 리터럴 | Microsoft Docs"
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
- string literals, syntax
- strings [C++], string literals
- literal strings, C
ms.assetid: 4b05523e-49a2-4900-b21a-754350af3328
caps.latest.revision: 11
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
ms.openlocfilehash: 2ca39273bff41d1a08d078445ddf8d8b56252db8
ms.contentlocale: ko-kr
ms.lasthandoff: 05/18/2017

---
# <a name="c-string-literals"></a>C 문자열 리터럴
"문자열 리터럴"은 큰따옴표(**" "**)로 묶은 소스 문자 집합의 문자 시퀀스입니다. 문자열 리터럴은 함께 사용될 경우 null로 끝나는 문자열을 형성하는 문자 시퀀스를 나타냅니다. 항상 와이드 문자열 리터럴의 접두어로 **L** 문자를 사용해야 합니다.  
  
## <a name="syntax"></a>구문  
 *string-literal*:  
 **"** *s-char-sequence* opt**"**  
  
 **L"** *s-char-sequence* opt**"**  
  
 *s-char-sequence*:  
 *s-char*  
  
 *s-char-sequence s-char*  
  
 *s-char*:  
 큰따옴표("), 백슬래시(\\) 또는 줄 바꿈 문자를 제외한 소스 문자 집합의 모든 멤버  
  
 *escape-sequence*  
  
 아래 예제는 단순 문자열 리터럴입니다.  
  
```  
char *amessage = "This is a string literal.";  
```  
  
 [이스케이프 시퀀스](../c-language/escape-sequences.md) 표에 나열된 모든 이스케이프 코드가 문자열 리터럴에서 유효합니다. 문자열 리터럴에서 큰따옴표를 표시하려면 **\\"** 이스케이프 시퀀스를 사용합니다. 작은따옴표(**'**)는 이스케이프 시퀀스 없이 나타낼 수 있습니다. 백슬래시(**\\**)는 문자열 내에 표시될 때 다른 하나의 백슬래시(**\\\\**)와 함께 표시되어야 합니다. 백슬래시가 줄 끝에 있으면 항상 줄 연속 문자로 해석됩니다.  
  
## <a name="see-also"></a>참고 항목  
 [C 요소](../c-language/elements-of-c.md)