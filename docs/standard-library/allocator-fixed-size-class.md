---
title: "allocator_fixed_size 클래스 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- allocators/stdext::allocators::allocator_fixed_size
- allocators::allocator_fixed_size
- allocators/stdext::allocator_fixed_size
- allocator_fixed_size
- stdext::allocators::allocator_fixed_size
dev_langs:
- C++
helpviewer_keywords:
- allocator_fixed_size class
ms.assetid: 138f3ef8-b0b3-49c3-9486-58f2213c172f
caps.latest.revision: 19
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
ms.translationtype: Machine Translation
ms.sourcegitcommit: 4ecf60434799708acab4726a95380a2d3b9dbb3a
ms.openlocfilehash: 95fdb03f48080c309b61df6f760d2d29a7e865ff
ms.contentlocale: ko-kr
ms.lasthandoff: 04/19/2017

---
# <a name="allocatorfixedsize-class"></a>allocator_fixed_size 클래스
[max_fixed_size](../standard-library/max-fixed-size-class.md)에 의해 관리되는 길이와 함께 [cache_freelist](../standard-library/cache-freelist-class.md) 형식의 캐시를 사용하여 `Type` 형식의 개체에 대한 저장소 할당 및 해제를 관리하는 개체를 설명합니다.  
  
## <a name="syntax"></a>구문  
  
```
template <class Type>  
class allocator_fixed_size;
```  
  
#### <a name="parameters"></a>매개 변수  
  
|매개 변수|설명|  
|---------------|-----------------|  
|`Type`|할당자에 의해 할당된 요소 형식입니다.|  
  
## <a name="remarks"></a>설명  
 [ALLOCATOR_DECL](../standard-library/allocators-functions.md#allocator_decl) 매크로는 다음 문에서 이 클래스를 `name` 매개 변수로서 전달합니다. `ALLOCATOR_DECL(CACHE_FREELIST(stdext::allocators::max_fixed_size<10>), SYNC_DEFAULT, allocator_fixed_size);`  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** \<allocators>  
  
 **네임스페이스:** stdext  
  
## <a name="see-also"></a>참고 항목  
 [\<allocators>](../standard-library/allocators-header.md)



