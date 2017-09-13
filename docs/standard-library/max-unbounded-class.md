---
title: "max_unbounded 클래스 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- allocators/stdext::max_unbounded
- stdext::max_unbounded
- max_unbounded
- allocators/stdext::max_unbounded::allocated
- allocators/stdext::max_unbounded::deallocated
- allocators/stdext::max_unbounded::full
- allocators/stdext::max_unbounded::released
- allocators/stdext::max_unbounded::saved
dev_langs:
- C++
helpviewer_keywords:
- max_unbounded class
ms.assetid: e34627a9-c231-4031-a483-cbb0514fff46
caps.latest.revision: 18
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.mt:
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
ms.sourcegitcommit: 66798adc96121837b4ac2dd238b9887d3c5b7eef
ms.openlocfilehash: c12c03d734b411767e7aeef1c2c541103e5ff286
ms.contentlocale: ko-kr
ms.lasthandoff: 04/29/2017

---
# <a name="maxunbounded-class"></a>max_unbounded 클래스
[freelist](../standard-library/freelist-class.md) 개체의 최대 길이를 제한하지 않는 [max 클래스](../standard-library/allocators-header.md) 개체를 설명합니다.  
  
## <a name="syntax"></a>구문  
  
```
class max_unbounded
```  
  
### <a name="member-functions"></a>멤버 함수  
  
|||  
|-|-|  
|[allocated](#allocated)|할당된 메모리 블록의 수를 늘립니다.|  
|[deallocated](#deallocated)|할당된 메모리 블록의 수를 줄입니다.|  
|[full](#full)|사용 가능한 목록에 더 많은 메모리 블록을 추가할지 여부를 지정하는 값을 반환합니다.|  
|[released](#released)|사용 가능한 목록에서 메모리 블록의 수를 줄입니다.|  
|[saved](#saved)|사용 가능한 목록에서 메모리 블록의 수를 늘립니다.|  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** \<allocators>  
  
 **네임스페이스:** stdext  
  
##  <a name="allocated"></a>  max_unbounded::allocated  
 할당된 메모리 블록의 수를 늘립니다.  
  
```
void allocated(std::size_t _Nx = 1);
```  
  
### <a name="parameters"></a>매개 변수  
  
|매개 변수|설명|  
|---------------|-----------------|  
|`_Nx`|증분 값입니다.|  
  
### <a name="remarks"></a>설명  
 이 멤버 함수는 아무 작업도 수행하지 않습니다. 이 멤버 함수는 `cache_freelist::allocate`에서 `new` 연산자를 성공적으로 호출할 때마다 호출됩니다. `_Nx` 인수는 청크에서 `new` 연산자가 할당한 메모리 블록의 수입니다.  
  
##  <a name="deallocated"></a>  max_unbounded::deallocated  
 할당된 메모리 블록의 수를 줄입니다.  
  
```
void deallocated(std::size_t _Nx = 1);
```  
  
### <a name="parameters"></a>매개 변수  
  
|매개 변수|설명|  
|---------------|-----------------|  
|`_Nx`|증분 값입니다.|  
  
### <a name="remarks"></a>설명  
 멤버 함수는 아무 작업도 수행하지 않습니다. 이 멤버 함수는 `cache_freelist::deallocate`에서 `delete` 연산자를 호출할 때마다 호출됩니다. `_Nx` 인수는 청크에서 `delete` 연산자가 할당 취소한 메모리 블록의 수입니다.  
  
##  <a name="full"></a>  max_unbounded::full  
 사용 가능한 목록에 더 많은 메모리 블록을 추가할지 여부를 지정하는 값을 반환합니다.  
  
```
bool full();
```  
  
### <a name="return-value"></a>반환 값  
 구성원 함수는 항상 `false`를 반환합니다.  
  
### <a name="remarks"></a>설명  
 이 멤버 함수는 `cache_freelist::deallocate`에서 호출됩니다. 호출에서 `true`를 반환하는 경우 `deallocate`는 메모리 블록을 사용 가능한 목록에 넣고, false를 반환하는 경우 `deallocate`는 `delete` 연산자를 호출하여 블록을 할당 취소합니다.  
  
##  <a name="released"></a>  max_unbounded::released  
 사용 가능한 목록에서 메모리 블록의 수를 줄입니다.  
  
```
void released();
```  
  
### <a name="remarks"></a>설명  
 이 멤버 함수는 아무 작업도 수행하지 않습니다. 현재 max 클래스의 `released` 멤버 함수는 사용 가능한 목록에서 메모리 블록을 제거할 때마다 `cache_freelist::allocate`에서 호출됩니다.  
  
##  <a name="saved"></a>  max_unbounded::saved  
 사용 가능한 목록에서 메모리 블록의 수를 늘립니다.  
  
```
void saved();
```  
  
### <a name="remarks"></a>설명  
 이 멤버 함수는 아무 작업도 수행하지 않습니다. 이 멤버 함수는 사용 가능한 목록에 메모리 블록을 넣을 때마다 `cache_freelist::deallocate`에서 호출됩니다.  
  
## <a name="see-also"></a>참고 항목  
 [\<allocators>](../standard-library/allocators-header.md)



