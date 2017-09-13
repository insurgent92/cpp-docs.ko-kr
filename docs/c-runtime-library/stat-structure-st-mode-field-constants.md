---
title: "_stat 구조체 st_mode 필드 상수 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- S_IFCHR
- S_IFDIR
- _S_IWRITE
- S_IFMT
- _S_IFDIR
- _S_IREAD
- S_IEXEC
- _S_IEXEC
- _S_IFMT
- S_IWRITE
- S_IFREG
- S_IREAD
- _S_IFCHR
- _S_IFREG
dev_langs:
- C++
helpviewer_keywords:
- S_IFDIR constant
- stat structure
- S_IWRITE constant
- S_IEXEC constant
- _S_IFREG constant
- S_IREAD constant
- stat structure, constants
- _S_IFMT constant
- st_mode field constants
- S_IFMT constant
- _S_IEXEC constant
- _S_IWRITE constant
- _S_IFDIR constant
- S_IFREG constant
- S_IFCHR constant
- _S_IREAD constant
- _S_IFCHR constant
ms.assetid: fd462004-7563-4766-8443-30b0a86174b6
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
ms.openlocfilehash: ebac26fce8a1717cd6d964e8cec6a5ce7e3c2d8f
ms.contentlocale: ko-kr
ms.lasthandoff: 05/18/2017

---
# <a name="stat-structure-stmode-field-constants"></a>_stat 구조체 st_mode 필드 상수
## <a name="syntax"></a>구문  
  
```  
  
#include <sys/stat.h>  
  
```  
  
## <a name="remarks"></a>설명  
 이러한 상수는 [_stat 구조](../c-runtime-library/standard-types.md)의 **st_mode** 필드에 있는 파일 형식을 나타내는 데 사용됩니다.  
  
 다음은 비트 마스크 상수에 대한 설명입니다.  
  
|상수|의미|  
|--------------|-------------|  
|`_S_IFMT`|파일 형식 마스크|  
|`_S_IFDIR`|디렉터리|  
|`_S_IFCHR`|특수 문자(설정된 경우 장치를 나타냄)|  
|`_S_IFREG`|기본|  
|`_S_IREAD`|읽기 권한, 소유자|  
|`_S_IWRITE`|쓰기 권한, 소유자|  
|`_S_IEXEC`|실행/검색 권한, 소유자|  
  
## <a name="see-also"></a>참고 항목  
 [_stat, _wstat 함수](../c-runtime-library/reference/stat-functions.md)   
 [_fstat, _fstat32, _fstat64, _fstati64, _fstat32i64, _fstat64i32](../c-runtime-library/reference/fstat-fstat32-fstat64-fstati64-fstat32i64-fstat64i32.md)   
 [표준 형식](../c-runtime-library/standard-types.md)   
 [전역 상수](../c-runtime-library/global-constants.md)