---
title: "&lt;condition_variable&gt; | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- <condition_variable>
dev_langs:
- C++
ms.assetid: 8567f7cc-20bd-42a7-9137-87c46f878009
caps.latest.revision: 19
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
ms.translationtype: Machine Translation
ms.sourcegitcommit: cc82b83860786ffc3f0aee73ede18ecadef16a7a
ms.openlocfilehash: 6002dcd4cd0fe35c99ce56a1d9fd3b5f3c23dd08
ms.contentlocale: ko-kr
ms.lasthandoff: 02/24/2017

---
# <a name="ltconditionvariablegt"></a>&lt;condition_variable&gt;
조건이 true가 될 때까지 대기하는 개체를 만드는 데 사용되는 [condition_variable](../standard-library/condition-variable-class.md) 및 [condition_variable_any](../standard-library/condition-variable-any-class.md) 클래스를 정의합니다.  
  
 이 헤더는 동시성 런타임(ConcRT)을 사용하므로 다른 ConcRT 메커니즘과 함께 사용할 수 있습니다. ConcRT에 대한 자세한 내용은 [동시성 런타임](../parallel/concrt/concurrency-runtime.md)을 참조하세요.  
  
## <a name="syntax"></a>구문  
  
```cpp  
#include <condition_variable>  
```  
  
> [!NOTE]
>  사용 하 여 컴파일되는 코드에서 **/clr**,이 헤더는 차단 됩니다.  
  
### <a name="remarks"></a>주의  
 조건 변수를 대기하는 코드에서는 `mutex`를 사용해야 합니다. 조건 변수를 대기하는 함수를 호출하기 전에 호출 스레드에서 `mutex`를 잠가야 합니다. 호출된 함수가 반환될 때 `mutex`가 잠깁니다. 스레드가 조건이 true가 될 때까지 대기하는 동안에는 `mutex`가 잠기지 않습니다. 예기치 않은 결과가 없도록 조건 변수를 대기하는 각 스레드는 동일한 `mutex` 개체를 사용해야 합니다.  
  
 `condition_variable_any` 형식의 개체는 모든 종류의 뮤텍스와 함께 사용할 수 있습니다. 사용되는 뮤텍스의 형식에서 `try_lock` 메서드를 제공할 필요가 없습니다. `condition_variable` 형식의 개체만 `unique_lock<mutex>` 형식의 뮤텍스와 함께 사용할 수 있습니다. 이 형식의 개체는 `condition_variable_any<unique_lock<mutex>>` 형식의 개체보다 빠를 수 있습니다.  
  
 이벤트를 대기하려면 먼저 뮤텍스를 잠근 후 조건 변수에 대한 `wait` 메서드 중 하나를 호출합니다. 다른 스레드가 조건 변수를 알릴 때까지 `wait`에서 블록을 호출합니다.  
  
 조건 변수를 대기 중인 스레드가 적절한 알림 없이 차단 해제될 때 *의사 대기 모드 해제*가 발생합니다. 이러한 의사 대기 모드 해제를 인식하기 위해 대기 함수에서 코드가 반환될 때 조건이 true가 될 때까지 대기하는 코드에서 해당 조건을 명시적으로 확인해야 합니다. 이는 보통 루프를 사용하여 수행됩니다. `wait(unique_lock<mutex>& lock, Predicate pred)`를 사용하여 이 루프를 자동으로 수행할 수 있습니다.  
  
```cpp  
while (condition is false)
    wait for condition variable;
```  
  
 `condition_variable_any` 및 `condition_variable` 클래스는 각기 조건을 대기하는 세 개의 메서드를 포함합니다.  
  
- `wait`는 제한 없는 시간 동안 대기합니다.  
  
- `wait_until`은 지정된 `time`까지 대기합니다.  
  
- `wait_for`는 지정된 `time interval` 동안 대기합니다.  
  
 이러한 각 메서드에는 두 개의 오버로드된 버전이 있습니다. 하나는 대기만 하다가 의사적으로 대기 모드를 해제할 수 있습니다. 다른 하나는 조건자를 정의하는 추가 템플릿 인수를 사용합니다. 조건자가 `true`가 될 때까지 메서드에서 반환하지 않습니다.  
  
 각 클래스에는 조건이 `true`가 되는 것을 조건 변수에 알리는 데 사용되는 두 가지 메서드가 있습니다.  
  
- `notify_one`은 조건 변수를 대기 중인 스레드 중 하나의 대기 모드를 해제합니다.  
  
- `notify_all`은 조건 변수를 대기 중인 모든 스레드의 대기 모드를 해제합니다.  
  
## <a name="see-also"></a>참고 항목  
 [헤더 파일 참조](../standard-library/cpp-standard-library-header-files.md)   
 [condition_variable 클래스](../standard-library/condition-variable-class.md)   
 [condition_variable_any 클래스](../standard-library/condition-variable-any-class.md)
