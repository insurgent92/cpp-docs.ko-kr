---
title: _setjmp3 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
apiname:
- _setjmp3
apilocation:
- msvcrt.dll
- msvcr90.dll
- msvcr110.dll
- msvcr80.dll
- msvcr110_clr0400.dll
- msvcr100.dll
- msvcr120.dll
apitype: DLLExport
f1_keywords:
- setjmp3
- _setjmp3
dev_langs:
- C++
helpviewer_keywords:
- _setjmp3 function
- setjmp3 function
ms.assetid: 6129c2f3-8bac-4fdb-a827-44e1eebba500
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
ms.openlocfilehash: 71a5963326e950c8e5c6aac629d1f428b189be18
ms.contentlocale: ko-kr
ms.lasthandoff: 05/18/2017

---
# <a name="setjmp3"></a>_setjmp3
내부 CRT 함수입니다. `setjmp` 함수의 새로운 구현입니다.  
  
## <a name="syntax"></a>구문  
  
```  
int _setjmp3(  
   OUT jmp_buf env,  
   int count,  
   (optional parameters)  
);  
```  
  
#### <a name="parameters"></a>매개 변수  
 [out] `env`  
 상태 정보 저장을 위한 버퍼 주소입니다.  
  
 [in] `count`  
 `DWORD`에 저장된 정보의 추가 `optional parameters` 수입니다.  
  
 [in] `optional parameters`  
 `setjmp` 내장 함수가 적용한 추가 데이터입니다. 첫 번째 `DWORD`는 추가 데이터를 해제한 다음 비휘발성 등록 상태로 반환하는 데 사용되는 함수 포인터입니다. 두 번째 `DWORD`는 복원할 시도 수준입니다. 모든 추가 데이터는 `jmp_buf`의 제네릭 데이터 배열에 저장됩니다.  
  
## <a name="return-value"></a>반환 값  
 항상 0을 반환합니다.  
  
## <a name="remarks"></a>설명  
 이 함수는 C++ 프로그램에서는 사용하지 마세요. C++을 지원하지 않는 내장 함수입니다. `setjmp`를 사용하는 방법에 대한 자세한 내용은 [setjmp/longjmp 사용](../cpp/using-setjmp-longjmp.md)을 참조하세요.  
  
## <a name="requirements"></a>요구 사항  
  
## <a name="see-also"></a>참고 항목  
 [사전순 함수 참조](../c-runtime-library/reference/crt-alphabetical-function-reference.md)   
 [setjmp](../c-runtime-library/reference/setjmp.md)