---
title: "bidirectional_iterator_tag 구조체 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- xutility/std::bidirectional_iterator_tag
- bidirectional_iterator_tag
dev_langs:
- C++
helpviewer_keywords:
- bidirectional_iterator_tag class
- bidirectional_iterator_tag struct
ms.assetid: 9ac06066-b8ae-44b6-bee4-b05855f6a31a
caps.latest.revision: 20
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
ms.sourcegitcommit: 2d05749ba2837a3879c91886b9266de47dd2ece6
ms.openlocfilehash: 33302a822cc36adf7f68d7cce29b678654aabb29
ms.contentlocale: ko-kr
ms.lasthandoff: 02/24/2017

---
# <a name="bidirectionaliteratortag-struct"></a>bidirectional_iterator_tag 구조체
양방향 반복기를 나타내는 **iterator_category** 함수에 반환 형식을 제공하는 클래스입니다.  
  
## <a name="syntax"></a>구문  
  
```
struct bidirectional_iterator_tag    : public forward_iterator_tag {};
```  
  
## <a name="remarks"></a>설명  
 범주 태그 클래스는 알고리즘 선택을 위한 컴파일 태그로 사용됩니다. 템플릿 함수는 컴파일 시 가장 효율적인 알고리즘을 사용할 수 있도록 해당 반복기 인수의 가장 구체적인 범주를 찾아야 합니다. `Iterator` 형식의 모든 반복기에 대해 `iterator_traits`< `Iterator`>:: **iterator_category**는 반복기 동작을 설명하는 가장 구체적인 범주 태그로 정의되어야 합니다.  
  
 **Iter**가 출력 반복기로 사용될 수 있는 개체를 설명할 경우 이 형식은 **iterator**\< **Iter**>:: **iterator_category**와 같습니다.  
  
## <a name="example"></a>예제  
 `bidirectional_iterator_tag` 사용 방법의 예는 [random_access_iterator_tag](../standard-library/random-access-iterator-tag-struct.md)를 참조하세요.  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** \<iterator>  
  
 **네임스페이스:** std  
  
## <a name="see-also"></a>참고 항목  
 [forward_iterator_tag 구조체](../standard-library/forward-iterator-tag-struct.md)   
 [C++ 표준 라이브러리의 스레드 보안](../standard-library/thread-safety-in-the-cpp-standard-library.md)   
 [C++ 표준 라이브러리 참조](../standard-library/cpp-standard-library-reference.md)



