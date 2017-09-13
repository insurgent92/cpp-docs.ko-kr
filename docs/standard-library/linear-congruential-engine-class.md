---
title: "linear_congruential_engine 클래스 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- linear_congruential_engine
- random/std::linear_congruential_engine
dev_langs:
- C++
helpviewer_keywords:
- linear_congruential_engine class
ms.assetid: 30e00ca6-1933-4701-9561-54f3e810a5a1
caps.latest.revision: 21
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
ms.openlocfilehash: bbb733e102af57627c00006816bb8d955877d0f8
ms.contentlocale: ko-kr
ms.lasthandoff: 04/19/2017

---
# <a name="linearcongruentialengine-class"></a>linear_congruential_engine 클래스
선형 합동 알고리즘에 따라 임의 시퀀스를 생성합니다.  
  
## <a name="syntax"></a>구문  
```  
class linear_congruential_engine{  
   public:  // types  
   typedef UIntType result_type;  
   // engine characteristics  
   static constexpr result_type multiplier = a;  
   static constexpr result_type increment = c;  
   static constexpr result_type modulus = m;  
   static constexpr result_type min() { return c == 0u  1u: 0u; }  
   static constexpr result_type max() { return m - 1u; }  
   static constexpr result_type default_seed = 1u;  
   // constructors and seeding functions  
   explicit linear_congruential_engine(result_type s = default_seed);
   template <class Sseq>  
   explicit linear_congruential_engine(Sseq& q);
   void seed(result_type s = default_seed);
   template <class Sseq>  
   void seed(Sseq& q);
   // generating functions  
   result_type operator()();
   void discard(unsigned long long z);
   };  
```  
#### <a name="parameters"></a>매개 변수  
 `UIntType`  
 부호가 없는 정수 결과 형식입니다. 가능한 형식은 [\<random>](../standard-library/random.md)을 참조하세요.  
  
 `A`  
 **승수**. **사전 조건**: 설명 섹션을 참조하세요.  
  
 `C`  
 **증분**. **사전 조건**: 설명 섹션을 참조하세요.  
  
 `M`  
 **모듈러스**. **사전 조건**: 설명을 참조하세요.  
  
## <a name="members"></a>멤버  
  
||||  
|-|-|-|  
|`linear_congruential_engine::linear_congruential_engine`|`linear_congruential_engine::min`|`linear_congruential_engine::discard`|  
|`linear_congruential_engine::operator()`|`linear_congruential_engine::max`|`linear_congruential_engine::seed`|  
  
 `default_seed`는 `1u`로 정의된 멤버 상수로, `linear_congruential_engine::seed` 및 단일 값 생성자의 기본 매개 변수 값으로 사용됩니다.  
  
 엔진 구성원에 대한 자세한 내용은 [\<random>](../standard-library/random.md)을 참조하세요.  
  
## <a name="remarks"></a>설명  
 `linear_congruential_engine` 템플릿 클래스는 가장 단순한 생성기 엔진이지만 가장 빠르거나 품질이 가장 뛰어나지는 않습니다. 이 엔진을 개선한 것이 [substract_with_carry_engine](../standard-library/subtract-with-carry-engine-class.md)입니다. 이러한 엔진 둘 다 [mersenne_twister_engine](../standard-library/mersenne-twister-engine-class.md)만큼 빠르거나 품질 결과가 뛰어나지는 않습니다.  
  
 이 엔진은 되풀이 관계(*period*) `x(i) = (A * x(i-1) + C) mod M`을 사용하여 사용자가 지정한 부호 없는 정수 형식의 값을 생성합니다.  
  
 `M`이 0이면 이 모듈러스 연산에 사용되는 값은 `numeric_limits<result_type>::max() + 1`입니다. 엔진의 상태는 반환되는 마지막 값이거나 `operator()`를 호출하지 않은 경우에는 시드 값입니다.  
  
 `M`이 0이 아니면 템플릿 인수 `A`와 `C`의 값이 `M`보다 작아야 합니다.  
  
 이 엔진에서 직접 생성기를 생성할 수 있더라도 다음의 미리 정의된 형식 정의 중 하나를 사용할 수 있습니다.  
  
 `minstd_rand0`: 1988 최소 표준 엔진입니다(Lewis, Goodman 및 Miller, 1969).  
  
```  
typedef linear_congruential_engine<unsigned int, 16807, 0, 2147483647> minstd_rand0;  
```  
  
 `minstd_rand`: 업데이트된 최소 표준 엔진 `minstd_rand0`입니다(Park, Miller 및 Stockmeyer, 1993).  
  
```  
typedef linear_congruential_engine<unsigned int, 48271, 0, 2147483647> minstd_rand;  
```  
  
 선형 합동 엔진 알고리즘에 대한 자세한 내용은 Wikipedia 문서 [Linear congruential generator](http://go.microsoft.com/fwlink/LinkId=402446)(선형 합동 발생기)를 참조하세요.  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** \<random>  
  
 **네임스페이스:** std  
  
## <a name="see-also"></a>참고 항목  
 [\<random>](../standard-library/random.md)


