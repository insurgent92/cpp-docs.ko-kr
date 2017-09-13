---
title: "입력 및 출력 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- c.io
dev_langs:
- C++
helpviewer_keywords:
- input routines
- I/O [CRT]
- I/O routines
- I/O [CRT], routines
- output routines
ms.assetid: 1c177301-e341-4ca0-aedc-0a87fe1c75ae
caps.latest.revision: 9
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
ms.openlocfilehash: 79ede2f4d96f0dd985b5b68cf83e641cbba10f3e
ms.contentlocale: ko-kr
ms.lasthandoff: 05/18/2017

---
# <a name="input-and-output"></a>입력 및 출력
I/O 함수는 파일 및 장치에서 데이터를 읽고 씁니다. 파일 I/O 연산은 텍스트 모드 또는 이진 모드로 수행됩니다. Microsoft 런타임 라이브러리에는 다음 세 가지 형식의 I/O 함수가 있습니다.  
  
-   [스트림 I/O](../c-runtime-library/stream-i-o.md) 함수는 데이터를 개별 문자 스트림으로 처리합니다.  
  
-   [하위 수준 I/O](../c-runtime-library/low-level-i-o.md) 함수는 스트림 I/O에서 제공하는 연산보다 낮은 수준의 연산에 대해 직접적으로 운영 체제를 호출합니다.  
  
-   [콘솔 및 포트 I/O](../c-runtime-library/console-and-port-i-o.md) 함수는 직접 콘솔(키보드 및 화면) 또는 I/O 포트(프린터 포트)에 읽거나 씁니다.  
  
    > [!NOTE]
    >  스트림 함수는 버퍼링되고 하위 수준 함수는 버퍼링되지 않으므로 이러한 두 형식의 함수는 일반적으로 호환되지 않습니다. 특정 파일 처리를 위해 단독으로 스트림 또는 하위 수준 함수를 사용합니다.  
  
## <a name="see-also"></a>참고 항목  
 [범주별 런타임 루틴](../c-runtime-library/run-time-routines-by-category.md)