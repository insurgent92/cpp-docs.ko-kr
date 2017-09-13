---
title: "subtract_with_carry_engine 클래스 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- subtract_with_carry_engine
- random/std::subtract_with_carry_engine
- random/std::subtract_with_carry_engine::default_seed
- random/std::subtract_with_carry_engine::discard
- random/std::subtract_with_carry_engine::min
- random/std::subtract_with_carry_engine::max
- random/std::subtract_with_carry_engine::seed
dev_langs:
- C++
helpviewer_keywords:
- subtract_with_carry_engine class
ms.assetid: 94a055f2-a620-4a22-ac34-c156924bab31
caps.latest.revision: 20
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
ms.sourcegitcommit: 4ecf60434799708acab4726a95380a2d3b9dbb3a
ms.openlocfilehash: c73401963b231883d26aa45590a9cad305b13875
ms.contentlocale: ko-kr
ms.lasthandoff: 04/19/2017

---
# <a name="subtractwithcarryengine-class"></a>subtract_with_carry_engine 클래스
subtract-with-carry(지연된 피보나치) 알고리즘을 사용하여 임의 시퀀스를 생성합니다.  
  
## <a name="syntax"></a>구문  
  
```  
template <class UIntType, size_t W, size_t S, size_t R>  
class subtract_with_carry_engine;  
```  
  
#### <a name="parameters"></a>매개 변수  
 `UIntType`  
 부호가 없는 정수 결과 형식입니다. 가능한 형식은 [\<random>](../standard-library/random.md)을 참조하세요.  
  
 `W`  
 **단어 크기**. 상태 시퀀스의 각 단어 크기입니다(비트). **사전 조건**: `0 < W ≤ numeric_limits<UIntType>::digits`  
  
 `S`  
 **짧은 지연**. 정수 값의 개수입니다. **사전 조건**: `0 < S < R`  
  
 `R`  
 **긴 지연**. 되풀이가 연속으로 발생했는지 확인합니다.  
  
## <a name="members"></a>멤버  
  
||||  
|-|-|-|  
|`subtract_with_carry_engine::subtract_with_carry_engine`|`subtract_with_carry_engine::min`|`subtract_with_carry_engine::discard`|  
|`subtract_with_carry_engine::operator()`|`subtract_with_carry_engine::max`|`subtract_with_carry_engine::seed`|  
|`default_seed`는 `19780503u`로 정의된 멤버 상수로, `subtract_with_carry_engine::seed` 및 단일 값 생성자의 기본 매개 변수 값으로 사용됩니다.|||  
  
 엔진 구성원에 대한 자세한 내용은 [\<random>](../standard-library/random.md)을 참조하세요.  
  
## <a name="remarks"></a>설명  
 `substract_with_carry_engine` 템플릿 클래스는 [linear_congruential_engine](../standard-library/linear-congruential-engine-class.md)보다 향상되었습니다. 이러한 엔진 둘 다 [mersenne_twister_engine](../standard-library/mersenne-twister-engine-class.md)만큼 빠르거나 품질 결과가 뛰어나지 않습니다.  
  
 이 엔진은 되풀이 관계(*period*) `x(i) = (x(i - R) - x(i - S) - cy(i - 1)) mod M`을 사용하여 사용자가 지정한 부호가 없는 정수 형식의 값을 생성합니다. 여기서 `cy(i)`의 값은 `x(i - S) - x(i - R) - cy(i - 1) < 0`인 경우 `1`이고, 그렇지 않으면 `0`입니다. `M`의 값은 `2`<sup>W</sup>입니다. 엔진의 상태는 전달 표시기 + `R` 값입니다. 이러한 값은 마지막 `R` 값으로 구성됩니다. `operator()`가 `R`번 호출된 경우 그렇습니다. 그렇지 않으면 반환된 `N` 값과 시드의 마지막 `R - N` 값으로 구성됩니다.  
  
 템플릿 인수 `UIntType`은 최대 `M - 1`까지 값을 보유할 수 있도록 충분히 커야 합니다.  
  
 엔진에서 직접 생성기를 생성할 수 있더라도 아래의 미리 정의된 typedef 중 하나를 사용할 수 있습니다.  
  
 `ranlux24_base`: `ranlux24`에 대한 기준으로 사용됩니다.                   
`typedef subtract_with_carry_engine<unsigned int, 24, 10, 24> ranlux24_base;`  
  
 `ranlux48_base`: `ranlux48`에 대한 기준으로 사용됩니다.                   
`typedef subtract_with_carry_engine<unsigned long long, 48, 5, 12> ranlux48_base;`  
  
 subtract_with_carry_engine 알고리즘에 대한 자세한 내용은 Wikipedia 문서 [지연된 피보나치 생성기](http://go.microsoft.com/fwlink/LinkId=402445)를 참조하세요.  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** \<random>  
  
 **네임스페이스:** std  
  
## <a name="see-also"></a>참고 항목  
 [\<random>](../standard-library/random.md)

