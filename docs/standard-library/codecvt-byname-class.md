---
title: "codecvt_byname 클래스 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- codecvt_byname
- xlocale/std::codecvt_byname
dev_langs:
- C++
helpviewer_keywords:
- codecvt_byname class
ms.assetid: b63b6c04-f60c-47b9-8e30-a933f24a8ffb
caps.latest.revision: 24
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
ms.openlocfilehash: cdf0ca3993103dc8070337b98bcacdb3e8c8b9d1
ms.contentlocale: ko-kr
ms.lasthandoff: 04/19/2017

---
# <a name="codecvtbyname-class"></a>codecvt_byname 클래스
지정된 로캘의 데이터 정렬 패싯으로 사용할 수 있는 개체를 설명하는 파생된 템플릿 클래스입니다. 이 클래스를 사용하여 변환과 관련된 문화 영역별 정보를 검색할 수 있습니다.  
  
## <a name="syntax"></a>구문  
  
```
template <class CharType, class Byte, class StateType>
class codecvt_byname: public codecvt<CharType, Byte, StateType> {
public:
    explicit codecvt_byname(
    const char* _Locname,
    size_t _Refs = 0);
```  
  
```
explicit codecvt_byname(
    const string& _Locname,
    size_t _Refs = 0);
```  
  
```
protected:
    virtual ~codecvt_byname();

};
```  
  
#### <a name="parameters"></a>매개 변수  
 `_Locname`  
 명명된 로캘입니다.  
  
 `_Refs`  
 초기 참조 개수입니다.  
  
## <a name="remarks"></a>설명  
 명명된 로캘이 생성되는 경우 byname 패싯이 자동으로 생성됩니다.  
  
 해당 동작은 명명된 로캘 `_Locname`에 따라 결정됩니다. 각 생성자는 [codecvt](../standard-library/codecvt-class.md)\<CharType, Byte, StateType>( `_Refs`)를 통해 해당 기본 개체를 초기화합니다.  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** \<locale>  
  
 **네임스페이스:** std  
  
## <a name="see-also"></a>참고 항목  
 [C++ 표준 라이브러리의 스레드 보안](../standard-library/thread-safety-in-the-cpp-standard-library.md)



