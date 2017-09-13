---
title: "ANSI C 규격 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- Ansi
dev_langs:
- C++
helpviewer_keywords:
- underscores, leading
- compatibility [C++], ANSI C
- compliance with ANSI C
- conventions [C++], Microsoft extensions
- underscores
- naming conventions [C++], Microsoft library
- ANSI [C++], C standard
- Microsoft extensions naming conventions
ms.assetid: 6be271bf-eecf-491a-a928-0ee2dd60e3b9
caps.latest.revision: 6
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
ms.translationtype: Human Translation
ms.sourcegitcommit: d6eb43b2e77b11f4c85f6cf7e563fe743d2a7093
ms.openlocfilehash: 7e6c5d4045f0b71890a34d845b898844ca550ca8
ms.contentlocale: ko-kr
ms.lasthandoff: 05/18/2017

---
# <a name="ansi-c-compliance"></a>ANSI C 규격
런타임 시스템(예: 함수, 매크로, 상수, 변수 및 형식 정의)의 모든 Microsoft 고유의 식별자에 대한 명명 규칙은 ANSI 규격입니다. 이 설명서에서는 ANSI/ISO C 표준을 따르는 모든 런타임 함수를 ANSI 호환으로 기록합니다. ANSI 호환 응용 프로그램은 이러한 ANSI 호환 함수를 사용해야 합니다.  
  
 Microsoft 고유의 함수 및 전역 변수 이름은 단일 밑줄로 시작합니다. 이러한 이름은 코드의 범위 내에서 로컬로만 재정의할 수 있습니다. 예를 들어 Microsoft 런타임 헤더 파일을 포함할 때 같은 이름의 지역 변수를 선언함으로써 로컬에서 `_open`이라는 이름의 Microsoft 고유의 함수를 재정의할 수 있습니다. 그러나 고유한 전역 함수나 전역 변수에는 이 이름을 사용할 수 없습니다.  
  
 Microsoft 매크로 및 매니페스트 상수의 이름은 두 개의 밑줄로 시작하거나 단일 선행 밑줄과 바로 이어지는 대문자로 시작합니다. 이러한 식별자의 범위는 절대입니다. 예를 들어 이러한 이유로 Microsoft 식별자 **_UPPER**를 사용할 수 없습니다.  
  
## <a name="see-also"></a>참고 항목  
 [호환성](../c-runtime-library/compatibility.md)