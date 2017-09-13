---
title: "부동 소수점 값 언더플로 | Microsoft Docs"
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
ms.assetid: 78af8016-643c-47db-b4f1-7f06cb4b243e
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
ms.openlocfilehash: 6383f383221bb18c1dc58223e7183531bfd3c2d2
ms.contentlocale: ko-kr
ms.lasthandoff: 05/18/2017

---
# <a name="underflow-of-floating-point-values"></a>부동 소수점 값 언더플로
**ANSI 4.5.1** 수학 함수가 정수 식 `errno`를 언더플로 범위 오류에 대한 `ERANGE` 매크로의 값으로 설정하는지 여부  
  
 부동 소수점 언더플로는 `errno` 식을 `ERANGE`로 설정하지 않습니다. 값이 0이고 결국 언더플로로 가까워지면 값이 0으로 설정됩니다.  
  
## <a name="see-also"></a>참고 항목  
 [라이브러리 함수](../c-language/library-functions.md)