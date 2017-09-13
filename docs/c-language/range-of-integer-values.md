---
title: "정수 값의 범위 | Microsoft Docs"
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
ms.assetid: 0e9c6161-8f3f-4bfb-9fcc-a6c8dc97d702
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
ms.sourcegitcommit: 3f91eafaf3b5d5c1b8f96b010206d699f666e224
ms.openlocfilehash: ac6e1783714c0aef62acecad24d345225a65e67e
ms.contentlocale: ko-kr
ms.lasthandoff: 04/01/2017

---
# <a name="range-of-integer-values"></a>정수 값의 범위
**ANSI 3.1.2.5** 다양한 형식의 정수 값에 대한 표현 및 집합  
  
 정수는 32비트(4바이트)를 포함합니다. 부호 있는 정수는 2의 보수 형식으로 표시됩니다. 최상위 비트는 음수에 대해서는 부호 1을, 양수와 0에 대해서는 0을 가집니다. 값은 아래와 같습니다.  
  
|형식|최소값 및 최대값|  
|----------|-------------------------|  
|**unsigned short**|0~65535|  
|`signed short`|-32768 ~ 32767|  
|`unsigned long`|0 ~ 4294967295|  
|**signed long**|-2147483648 ~ 2147483647|  
  
## <a name="see-also"></a>참고 항목  
 [정수](../c-language/integers.md)