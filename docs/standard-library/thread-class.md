---
title: "thread 클래스 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- thread/std::thread
- thread/std::thread::id Class
- thread/std::thread::thread
- thread/std::thread::detach
- thread/std::thread::get_id
- thread/std::thread::hardware_concurrency
- thread/std::thread::join
- thread/std::thread::joinable
- thread/std::thread::native_handle
- thread/std::thread::swap
dev_langs:
- C++
ms.assetid: df249bc7-ff81-4ff9-a6d6-5e3d9a8f56a1
caps.latest.revision: 16
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
ms.sourcegitcommit: 66798adc96121837b4ac2dd238b9887d3c5b7eef
ms.openlocfilehash: b1c5282d284a70917c6c14511bacda305180d778
ms.contentlocale: ko-kr
ms.lasthandoff: 04/29/2017

---
# <a name="thread-class"></a>thread 클래스
응용 프로그램 내의 실행 스레드를 관찰하고 관리하는 데 사용되는 개체를 정의합니다.  
  
## <a name="syntax"></a>구문  
  
```
class thread;
```  
  
## <a name="remarks"></a>설명  
 `thread` 개체를 사용하면 응용 프로그램 내의 실행 스레드를 관찰하고 관리할 수 있습니다. 기본 생성자를 사용하여 만드는 스레드 개체는 실행 스레드와 연결되지 않습니다. 호출 가능 개체를 사용하여 생성되는 스레드 개체는 새 실행 스레드를 만들고 해당 스레드의 호출 가능 개체를 호출합니다. 스레드 개체는 이동할 수는 있지만 복사할 수는 없습니다. 따라서 실행 스레드는 하나만 스레드 개체에만 연결할 수 있습니다.  
  
 모든 실행 스레드에는 `thread::id` 형식의 고유 식별자가 있습니다. `this_thread::get_id` 함수는 호출 스레드의 식별자를 반환합니다. `thread::get_id` 구성원 함수는 스레드 개체가 관리하는 스레드의 식별자를 반환합니다. 기본 생성 스레드 개체의 경우 `thread::get_id` 메서드는 모든 기본 생성 스레드 개체에 대해서는 동일하고 호출 시에 조인할 수 실행 스레드에 대해 `this_thread::get_id`에서 반환하는 값과는 다른 값이 포함된 개체를 반환합니다.  
  
## <a name="members"></a>멤버  
  
### <a name="public-classes"></a>public 클래스  
  
|이름|설명|  
|----------|-----------------|  
|[thread::id 클래스](#id_class)|관련 스레드를 고유하게 식별합니다.|  
  
### <a name="public-constructors"></a>Public 생성자  
  
|이름|설명|  
|----------|-----------------|  
|[thread](#thread)|`thread` 개체를 생성합니다.|  
  
### <a name="public-methods"></a>Public 메서드  
  
|이름|설명|  
|----------|-----------------|  
|[분리](#detach)|`thread` 개체에서 관련 스레드를 분리합니다.|  
|[get_id](#get_id)|관련 스레드의 고유 식별자를 반환합니다.|  
|[hardware_concurrency](#hardware_concurrency)|정적. 하드웨어 스레드 컨텍스트 수의 추정치를 반환합니다.|  
|[join](#join)|관련 스레드가 완료될 때까지 차단합니다.|  
|[참가할 수 있는](#joinable)|관련 스레드가 조인 가능한지를 지정합니다.|  
|[native_handle](#native_handle)|뮤텍스 핸들을 나타내는 구현별 형식을 반환합니다.|  
|[swap](#swap)|개체 상태를 지정된 `thread` 개체와 바꿉니다.|  
  
### <a name="public-operators"></a>Public 연산자  
  
|이름|설명|  
|----------|-----------------|  
|[thread::operator=](#op_eq)|현재 `thread` 개체에 스레드를 연결합니다.|  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** \<스레드 >  
  
 **네임스페이스:** std  
  
##  <a name="detach"></a>thread:: detach
 관련 스레드를 분리합니다. 종료 시에는 운영 체제가 스레드 리소스를 해제합니다.  
  
```
void detach();
```  
  
### <a name="remarks"></a>설명  
 `detach`에 대한 호출 이후 [get_id](#get_id)를 후속 호출하면 [id](#id_class)가 반환됩니다.  
  
 호출 개체와 연결된 스레드를 조인할 수 없는 경우 함수는 오류 코드가 `invalid_argument`인 [system_error](../standard-library/system-error-class.md)를 throw합니다.  
  
 호출 개체와 연결된 스레드가 유효하지 않은 경우 함수는 오류 코드가 `no_such_process`인 `system_error`를 throw합니다.  
  
##  <a name="get_id"></a>thread:: get_id
 연결된 스레드에 대한 고유 식별자를 반환합니다.  
  
```
id get_id() const noexcept;
```  
  
### <a name="return-value"></a>반환 값  
 연결된 스레드를 고유하게 식별하는 [thread::id](#id_class) 개체이거나, 개체에 스레드가 연결되어 있지 않은 경우 `thread::id()`입니다.  
  
##  <a name="hardware_concurrency"></a>thread:: hardware_concurrency
 하드웨어 스레드 컨텍스트 수의 추정치를 반환하는 정적 메서드입니다.  
  
```
static unsigned int hardware_concurrency() noexcept;
```  
  
### <a name="return-value"></a>반환 값  
 하드웨어 스레드 컨텍스트 수의 추정치입니다. 값이 계산할 수 없는 상태이거나 올바르게 정의되어 있지 않으면 이 메서드는 0을 반환합니다.  
  
##  <a name="id_class"></a>  thread::id 클래스  
 프로세스에서 각 실행 스레드에 대한 고유 식별자를 반환합니다.  
  
```
class thread::id {
    id() noexcept;
};
```  
  
### <a name="remarks"></a>설명  
 기본 생성자는 모든 기존 스레드에 대해 `thread::id` 개체와 비교하여 같지 않은 개체를 생성합니다.  
  
 모든 기본 생성 `thread::id` 개체의 비교 결과는 같습니다.  
  
##  <a name="join"></a>thread:: join
 호출 개체와 연결된 실행 스레드가 완료될 때까지 차단합니다.  
  
```
void join();
```  
  
### <a name="remarks"></a>설명  
 호출이 성공하면 호출 개체에 대한 [get_id](#get_id) 후속 호출에서는 기존 스레드의 `thread::id`와 비교할 때 같지 않은 기본 [thread::id](#id_class)가 반환됩니다. 호출이 성공하지 않으면 `get_id`에서 반환되는 값은 변경되지 않습니다.  
  
##  <a name="joinable"></a>thread:: joinable
 관련 스레드가 *조인 가능*한지를 지정합니다.  
  
```
bool joinable() const noexcept;
```  
  
### <a name="return-value"></a>반환 값  
 관련 스레드가 *조인 가능*하면 `true`이고 그렇지 않으면 `false`입니다.  
  
### <a name="remarks"></a>설명  
 스레드 개체는 `get_id() != id()`인 경우 *조인 가능*합니다.  
  
##  <a name="native_handle"></a>thread:: native_handle
 뮤텍스 핸들을 나타내는 구현별 형식을 반환합니다. 스레드 핸들은 구현별 방식으로 사용할 수 있습니다.  
  
```
native_handle_type native_handle();
```  
  
### <a name="return-value"></a>반환 값  
 `native_handle_type`은 `void *`로 캐스팅된 Win32 `HANDLE`로 정의됩니다.  
  
##  <a name="op_eq"></a>  thread::operator=  
 지정한 개체의 스레드를 현재 개체에 연결합니다.  
  
```
thread& operator=(thread&& Other) noexcept;
```  
  
### <a name="parameters"></a>매개 변수  
 `Other`  
 `thread` 개체입니다.  
  
### <a name="return-value"></a>반환 값  
 `*this`  
  
### <a name="remarks"></a>설명  
 호출 개체가 조인 가능하면 메서드는 detach를 호출합니다.  
  
 연결이 설정되면 `Other`는 기본 생성 상태로 설정됩니다.  
  
##  <a name="swap"></a>thread:: swap
 개체 상태를 지정된 `thread` 개체의 상태와 바꿉니다.  
  
```
void swap(thread& Other) noexcept;
```  
  
### <a name="parameters"></a>매개 변수  
 `Other`  
 `thread` 개체입니다.  
  
##  <a name="thread"></a>  thread::thread 생성자  
 `thread` 개체를 생성합니다.  
  
```
thread() noexcept;
template <class Fn, class... Args>
explicit thread(Fn&& F, Args&&... A);

thread(thread&& Other) noexcept;
```  
  
### <a name="parameters"></a>매개 변수  
 `F`  
 스레드에 의해 실행되는 응용 프로그램 정의 함수  
  
 `A`  
 `F`에 전달할 인수의 목록  
  
 `Other`  
 기존 `thread` 개체입니다.  
  
### <a name="remarks"></a>설명  
 첫 번째 생성자는 실행 스레드와 연결되지 않는 개체를 생성합니다. 생성된 개체에 대한 `get_id` 호출에서 반환되는 값은 `thread::id()`입니다.  
  
 두 번째 생성자는 새 실행 스레드와 연결되며 [\<functional>](../standard-library/functional.md)에 정의된 의사 함수 `INVOKE`를 실행하는 개체를 생성합니다. 새 스레드를 시작할 수 있는 리소스가 부족한 경우 함수는 오류 코드가 `resource_unavailable_try_again`인 [system_error](../standard-library/system-error-class.md) 개체를 throw합니다. `F` 호출이 확인할 수 없는 예외로 인해 종료되면 [terminate](../standard-library/exception-functions.md#terminate)가 호출됩니다.  
  
 세 번째 생성자는 `Other`에 연결된 스레드와 연결되는 개체를 생성합니다. 그러면 `Other`는 기본 생성 상태로 설정됩니다.  
  
## <a name="see-also"></a>참고 항목  
 [헤더 파일 참조](../standard-library/cpp-standard-library-header-files.md)   
 [\<thread>](../standard-library/thread.md)



