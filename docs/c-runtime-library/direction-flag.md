---
title: "방향 플래그 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- c.flags
dev_langs:
- C++
helpviewer_keywords:
- direction flag
ms.assetid: 0836b4af-dbbb-4ab8-a4b2-156f2e2099e2
caps.latest.revision: 7
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
ms.openlocfilehash: 8c1595b20e9f601bb5a86c68e63d9176e86e7b96
ms.contentlocale: ko-kr
ms.lasthandoff: 05/18/2017

---
# <a name="direction-flag"></a>방향 플래그
방향 플래그는 Intel 80x86 프로세스와 관련된 CPU 플래그입니다. 이 플래그는 MOVS, MOVSD, MOVSW 등과 같은 REP(반복) 접두사를 사용하는 모든 어셈블리 명령에 적용됩니다. 해당되는 명령에 제공되는 주소는 방향 플래그가 지워지면 증가합니다.  
  
 C 런타임 루틴은 방향 플래그가 지워졌다고 가정합니다. C 런타임 함수와 함께 다른 함수를 사용하는 경우 기타 함수에서 방향 플래그를 그대로 두거나 원래 상태로 복원하도록 해야 합니다. 방향 플래그가 입력될 때 명확하도록 예상하면 보다 빠르고 효율적인 런타임 코드가 생성됩니다.  
  
 문자열 조작 및 버퍼 조작 루틴과 같은 C 런타임 라이브러리 함수는 방향 플래그가 명확하도록 예상합니다.  
  
## <a name="see-also"></a>참고 항목  
 [CRT 라이브러리 기능](../c-runtime-library/crt-library-features.md)