---
title: "_get_output_format | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
apiname:
- _get_output_format
apilocation:
- msvcr110_clr0400.dll
- msvcr100.dll
- msvcr80.dll
- msvcrt.dll
- msvcr90.dll
- msvcr120.dll
- msvcr110.dll
apitype: DLLExport
f1_keywords:
- get_output_format
- _get_output_format
dev_langs:
- C++
helpviewer_keywords:
- output formatting
- get_output_format function
- _get_output_format function
ms.assetid: 0ce42f3b-3479-41c4-bcbf-1d21f7ee37e7
caps.latest.revision: 13
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.ht:
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- ru-ru
- zh-cn
- zh-tw
translation.priority.mt:
- cs-cz
- pl-pl
- pt-br
- tr-tr
ms.translationtype: Human Translation
ms.sourcegitcommit: e257f037a05c45f5b98e64ea55bd125af443b0be
ms.openlocfilehash: 389704142fe6d6f5806542cd2bdf6cdd4482172b
ms.contentlocale: ko-kr
ms.lasthandoff: 03/30/2017

---
# <a name="getoutputformat"></a>_get_output_format
출력 형식 플래그의 현재 값을 가져옵니다.  
  
> [!IMPORTANT]
>  이 함수는 사용되지 않습니다. Visual Studio 2015부터 CRT에서 사용할 수 없습니다.  
  
## <a name="syntax"></a>구문  
  
```  
unsigned int _get_output_format();  
```  
  
## <a name="return-value"></a>반환 값  
 출력 형식 플래그의 현재 값입니다.  
  
## <a name="remarks"></a>설명  
 출력 형식 플래그는 형식이 지정된 I/O의 기능을 제어합니다. 현재 플래그는 두 가지 가능한 값인 0과 `_TWO_DIGIT_EXPONENT`를 사용합니다. `_TWO_DIGIT_EXPONENT` 가 설정된 경우 부동 소수점 숫자는 세 번째 숫자가 지수의 크기에 따라 필요한 경우가 아닌 한 지수에 두 자리 숫자로 인쇄됩니다. 플래그가 0이면 부동 소수점 출력은 필요한 경우 0을 사용하여 세 자리에 값을 채워 지수의 세 자리를 표시합니다.  
  
## <a name="requirements"></a>요구 사항  
  
|루틴|필수 헤더|  
|-------------|---------------------|  
|`_get_output_format`|\<stdio.h>|  
  
 호환성에 대한 자세한 내용은 소개에서 [호환성](../c-runtime-library/compatibility.md)을 참조하세요.  
  
## <a name="see-also"></a>참고 항목  
[형식 사양 구문: printf 및 wprintf 함수](../c-runtime-library/format-specification-syntax-printf-and-wprintf-functions.md)  
 [printf, _printf_l, wprintf, _wprintf_l](../c-runtime-library/reference/printf-printf-l-wprintf-wprintf-l.md)   
 [printf_s, _printf_s_l, wprintf_s, _wprintf_s_l](../c-runtime-library/reference/printf-s-printf-s-l-wprintf-s-wprintf-s-l.md)   
 [_set_output_format](../c-runtime-library/set-output-format.md)  
