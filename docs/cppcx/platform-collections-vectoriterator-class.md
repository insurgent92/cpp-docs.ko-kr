---
title: "Platform::Collections::VectorIterator 클래스 | Microsoft Docs"
ms.custom: ""
ms.date: "12/30/2016"
ms.prod: "windows-client-threshold"
ms.technology: ""
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "language-reference"
f1_keywords: 
  - "collection/Platform::Collections::VectorIterator"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "VectorIterator 클래스"
ms.assetid: d531cb42-27e0-48a6-bf5e-c265891a18ff
caps.latest.revision: 7
author: "ghogen"
ms.author: "ghogen"
manager: "ghogen"
caps.handback.revision: 7
---
# Platform::Collections::VectorIterator 클래스
[!INCLUDE[wrt](../cppcx/includes/wrt-md.md)] IVector 인터페이스에서 파생된 개체에 대한 표준 템플릿 라이브러리 반복자를 제공합니다.  
  
 VectorIterator는 VectorProxy\<T\> 형식의 요소를 저장하는 프록시 반복기입니다. 그러나 프록시 개체는 사용자 코드에 거의 표시되지 않습니다. 자세한 내용은 [컬렉션\(C\+\+\/CX\)](../cppcx/collections-c-cx.md)을 참조하세요.  
  
## 구문  
  
```  
template <  
   typename T  
>  
class VectorIterator;  
```  
  
#### 매개 변수  
 `T`  
 VectorIterator 템플릿 클래스의 형식 이름입니다.  
  
## 멤버  
  
### 공용 Typedefs  
  
|이름|설명|  
|--------|--------|  
|`difference_type`|포인터 차이\(ptrdiff\_t\)입니다.|  
|`iterator_category`|임의 액세스 반복기의 범주입니다\(::std::random\_access\_iterator\_tag\).|  
|`pointer`|VectorIterator의 구현에 필요한 내부 형식 Platform::Collections::Details::VectorProxy\<T\>에 대한 포인터입니다.|  
|`reference`|VectorIterator의 구현에 필요한 내부 형식 Platform::Collections::Details::VectorProxy\<T\>에 대한 참조입니다.|  
|`value_type`|`T` 형식 이름입니다.|  
  
### Public 생성자  
  
|이름|설명|  
|--------|--------|  
|[VectorIterator::VectorIterator 생성자](../cppcx/vectoriterator-vectoriterator-constructor.md)|VectorIterator 클래스의 새 인스턴스를 초기화합니다.|  
  
### Public 연산자  
  
|이름|설명|  
|--------|--------|  
|[VectorIterator::operator\- 연산자](../cppcx/vectoriterator-operator-minus-operator.md)|현재 반복기에서 지정된 요소 수를 빼서 새 반복기를 계산하거나 현재 반복기에서 지정된 반복기를 빼서 반복기 간 요소 수 차이를 계산합니다.|  
|[VectorIterator::operator\-\- 연산자](../cppcx/vectoriterator-operator-decrement-operator.md)|현재 VectorIterator를 감소시킵니다.|  
|[VectorIterator::operator\!\= 연산자](../cppcx/vectoriterator-operator-inequality-operator.md)|현재 VectorIterator가 지정된 VectorIterator와 같지 않은지 여부를 나타냅니다.|  
|[VectorIterator::operator\* 연산자](../cppcx/vectoriterator-operator-dereference-operator.md)|현재 VectorIterator가 지정하는 요소에 대한 참조를 검색합니다.|  
|[VectorIterator::operatorOperator](../cppcx/vectoriterator-operatoroperator.md)|현재 VectorIterator에서 지정된 치환에 해당하는 요소에 대한 참조를 검색합니다.|  
|[\(DELETE\) VectorIterator::operator\+ 연산자](http://msdn.microsoft.com/ko-kr/b0b1af2c-e2a8-4876-99dc-7351bfc46ce4)|지정된 VectorIterator에서 지정된 치환에 해당하는 요소를 참조하는 VectorIterator를 반환합니다.|  
|[VectorIterator::operator\+\+ 연산자](../cppcx/vectoriterator-operator-increment-operator.md)|현재 VectorIterator를 증가시킵니다.|  
|[VectorIterator::operator\+\= 연산자](../cppcx/vectoriterator-operator-plus-assign-operator.md)|지정된 치환으로 현재 VectorIterator를 늘립니다.|  
|[VectorIterator::operator\< 연산자](../cppcx/vectoriterator-operator-less-than-operator.md)|현재 VectorIterator가 지정된 VectorIterator보다 작은지 여부를 나타냅니다.|  
|[VectorIterator::operator\<\= 연산자](../cppcx/vectoriterator-operator-less-than-or-equals-operator.md)|현재 VectorIterator가 지정된 VectorIterator보다 작거나 같은지 여부를 나타냅니다.|  
|[VectorIterator::operator\-\= 연산자](../cppcx/vectoriterator-operator-subtract-assign-operator.md)|지정된 치환으로 현재 VectorIterator를 줄입니다.|  
|[VectorIterator::operator\=\= 연산자](../cppcx/vectoriterator-operator-equality-operator.md)|현재 VectorIterator가 지정된 VectorIterator와 같은지 여부를 나타냅니다.|  
|[VectorIterator::operator\> 연산자](../cppcx/vectoriterator-operator-greater-than-operator.md)|현재 VectorIterator가 지정된 VectorIterator보다 큰지 여부를 나타냅니다.|  
|[VectorIterator::operator\-\> 연산자](../cppcx/vectoriterator-operator-arrow-operator.md)|현재 VectorIterator가 참조하는 요소의 주소를 검색합니다.|  
|[VectorIterator::operator\>\= 연산자](../cppcx/vectoriterator-operator-greater-than-or-equal-operator.md)|현재 VectorIterator가 지정된 VectorIterator보다 크거나 같은지 여부를 나타냅니다.|  
  
## 상속 계층  
 `VectorIterator`  
  
## 요구 사항  
 **헤더:** collection.h  
  
 **네임스페이스:** Platform::Collections  
  
## 참고 항목  
 [\(NOTINBUILD\) Platform 네임스페이스](http://msdn.microsoft.com/ko-kr/f3ce3eab-028c-4204-ba9f-9ab8af17c8c4)