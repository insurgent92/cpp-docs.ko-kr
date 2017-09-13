---
title: "변환: 진단 | Microsoft Docs"
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
ms.assetid: 3730ca7c-0147-452d-bd4a-6a1e97e9793e
caps.latest.revision: 6
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
ms.openlocfilehash: 525f8c235a4c2500b09ac37a050d4b57fadc8fb9
ms.contentlocale: ko-kr
ms.lasthandoff: 05/18/2017

---
# <a name="translation-diagnostics"></a>변환: 진단
**ANSI 2.1.1.3** 진단 식별 방법  
  
 Microsoft C는 다음의 경우에 형식에서 오류 메시지를 생성합니다.  
  
```  
  
filename( line-number ) : diagnostic Cnumbermessage  
```  
  
 *파일 이름*이 오류가 발견된 소스 파일의 이름일 경우, *줄 번호*가 컴파일러 오류가 발견된 줄 번호일 경우, `diagnostic`이 "오류" 또는 "경고"일 경우, `number`가 오류 또는 경고를 식별하는 고유한 네 자리 디지털 숫자(**C** 뒤에 위치, 구문 설명 참조)일 경우, `message`가 설명 메시지일 경우입니다.  
  
## <a name="see-also"></a>참고 항목  
 [Implementation-Defined Behavior](../c-language/implementation-defined-behavior.md)