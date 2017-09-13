---
title: "예외 처리 루틴 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- c.exceptions
dev_langs:
- C++
helpviewer_keywords:
- exception handling, routines
ms.assetid: f60548c6-850a-4e1e-a79b-a2a6a541ab62
caps.latest.revision: 8
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
ms.sourcegitcommit: e257f037a05c45f5b98e64ea55bd125af443b0be
ms.openlocfilehash: 3dd5d8dd77f2b62a6b0ea52e7d056b3d779cd2f4
ms.contentlocale: ko-kr
ms.lasthandoff: 03/30/2017

---
# <a name="exception-handling-routines"></a>예외 처리 루틴
C++ 예외 처리 함수를 사용하여 프로그램 실행 중에 예기치 않은 이벤트에서 복구할 수 있습니다.  
  
### <a name="exception-handling-functions"></a>예외 처리 함수  
  
|함수|기능|  
|--------------|---------|  
|[_set_se_translator](../c-runtime-library/reference/set-se-translator.md)|Win32 예외(C 구조적 예외)를 C++ 형식 예외로 처리|  
|[set_terminate](../c-runtime-library/reference/set-terminate-crt.md)|`terminate`로 호출할 자체 종료 루틴을 설치합니다.|  
|[set_unexpected](../c-runtime-library/reference/set-unexpected-crt.md)|`unexpected`로 호출할 자체 종료 함수를 설치합니다.|  
|[terminate](../c-runtime-library/reference/terminate-crt.md)|예외가 throw된 후에 특정 상황에서 자동으로 호출됩니다. `terminate` 함수는 `abort` 또는`set_terminate`를 사용하여 지정한 함수를 호출합니다.|  
|[unexpected](../c-runtime-library/reference/unexpected-crt.md)|`terminate`를 사용하여 `set_unexpected` 또는 사용자가 지정하는 함수를 호출합니다. `unexpected` 함수는 현재 Microsoft C++ 예외 처리 구현에서 사용되지 않습니다.|  
  
## <a name="see-also"></a>참고 항목  
 [범주별 런타임 루틴](../c-runtime-library/run-time-routines-by-category.md)