---
title: "independent_bits_engine 클래스 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- independent_bits_engine
- random/std::independent_bits_engine
dev_langs:
- C++
helpviewer_keywords:
- independent_bits_engine class
ms.assetid: 889e9a82-f457-49a7-9d2e-26e0fc3cd907
caps.latest.revision: 17
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
ms.openlocfilehash: 9a4052e44457b08f7d74f3591bd8665f0679c9a5
ms.contentlocale: ko-kr
ms.lasthandoff: 04/19/2017

---
# <a name="independentbitsengine-class"></a>independent_bits_engine 클래스
기본 엔진에서 반환한 값의 비트를 다시 압축하여 지정된 수의 비트를 사용하여 숫자의 임의 시퀀스를 생성합니다.  
  
## <a name="syntax"></a>구문  
  
```  
template <class Engine, size_t W, class UIntType>  
class independent_bits_engine;  
```  
  
### <a name="parameters"></a>매개 변수  
 `Engine`  
 기본 엔진 유형입니다.  
  
 `W`  
 **단어 크기**. 생성된 각 수의 크기입니다(비트). **사전 조건**: `0 < W ≤ numeric_limits<UIntType>::digits`  
  
 `UIntType`  
 부호가 없는 정수 결과 형식입니다. 가능한 형식은 [\<random>](../standard-library/random.md)을 참조하세요.  
  
## <a name="members"></a>멤버  
  
||||  
|-|-|-|  
|`independent_bits_engine::independent_bits_engine`|`independent_bits_engine::base`|`independent_bits_engine::discard`|  
|`independent_bits_engine::operator()`|`independent_bits_engine::base_type`|`independent_bits_engine::seed`|  
  
 엔진 구성원에 대한 자세한 내용은 [\<random>](../standard-library/random.md)을 참조하세요.  
  
## <a name="remarks"></a>설명  
 이 템플릿 클래스는 기본 엔진에서 반환하는 값의 비트를 다시 압축하여 `W` 비트 값을 생성하는 *엔진 어댑터*에 대해 설명합니다.  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** \<random>  
  
 **네임스페이스:** std  
  
## <a name="see-also"></a>참고 항목  
 [\<random>](../standard-library/random.md)

