---
title: "_CIsin | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
apiname:
- _CIsin
apilocation:
- msvcr80.dll
- msvcr100.dll
- msvcrt.dll
- msvcr110.dll
- msvcr120.dll
- msvcr90.dll
- msvcr110_clr0400.dll
apitype: DLLExport
f1_keywords:
- CIsin
- _CIsin
dev_langs:
- C++
helpviewer_keywords:
- _CIsin intrinsic
- CIsin intrinsic
ms.assetid: f215f39a-2341-4f1c-ba8e-cb522451ceb2
caps.latest.revision: 5
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
ms.sourcegitcommit: d6eb43b2e77b11f4c85f6cf7e563fe743d2a7093
ms.openlocfilehash: 589252c41b8acef0555322dcb1f006863a86f113
ms.contentlocale: ko-kr
ms.lasthandoff: 05/18/2017

---
# <a name="cisin"></a>_CIsin
스택 상위 값의 사인을 계산합니다.  
  
## <a name="syntax"></a>구문  
  
```  
void __cdecl _CIsin();  
```  
  
## <a name="remarks"></a>설명  
 이 버전의 `sin` 함수는 컴파일러가 이해할 수 있는 특별한 호출 규칙을 가집니다. 복사본이 생성되지 않도록 하며 레지스터 할당을 돕기 때문에 실행 속도를 높입니다.  
  
 결과 값이 스택의 맨 위에 푸시됩니다.  
  
## <a name="requirements"></a>요구 사항  
 **플랫폼:** x86  
  
## <a name="see-also"></a>참고 항목  
 [사전순 함수 참조](../c-runtime-library/reference/crt-alphabetical-function-reference.md)   
 [sin, sinf, sinl, sinh, sinhf, sinhl](../c-runtime-library/reference/sin-sinf-sinl-sinh-sinhf-sinhl.md)