---
title: "_bstr_t::_bstr_t | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "language-reference"
f1_keywords: 
  - "_bstr_t::_bstr_t"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "_bstr_t 클래스"
  - "_bstr_t 메서드"
  - "BSTR 개체"
ms.assetid: 116d994e-5a72-4351-afbe-866c80b4c165
caps.latest.revision: 10
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 10
---
# _bstr_t::_bstr_t
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

**Microsoft 전용**  
  
 `_bstr_t` 개체를 생성합니다.  
  
## 구문  
  
```  
_bstr_t( ) throw( );   
_bstr_t(  
   const _bstr_t& s1   
) throw( );  
_bstr_t(  
   const char* s2   
);  
_bstr_t(  
   const wchar_t* s3   
);  
_bstr_t(  
   const _variant_t& var   
);  
_bstr_t(  
   BSTR bstr,  
   bool fCopy   
);  
```  
  
#### 매개 변수  
 `s1`  
 복사할 `_bstr_t` 개체입니다.  
  
 `s2`  
 멀티바이트 문자열입니다.  
  
 `s3`  
 유니코드 문자열입니다.  
  
 `var`  
 [\_variant\_t](../cpp/variant-t-class.md) 개체입니다.  
  
 `bstr`  
 기존 `BSTR` 개체입니다.  
  
 `fCopy`  
 `false`인 경우 `bstr` 인수는 `SysAllocString`을 호출하여 복사본을 만들지 않고 새 개체에 연결됩니다.  
  
## 설명  
 다음 표는 `_bstr_t` 생성자에 대해 설명합니다.  
  
|생성자|설명|  
|---------|--------|  
|`_bstr_t( )`|null `BSTR` 개체를 캡슐화하는 기본 `_bstr_t` 개체를 구성합니다.|  
|`_bstr_t( _bstr_t&`  `s1`  `)`|`_bstr_t` 개체를 다른 개체의 복사본으로 생성합니다.<br /><br /> 이 *shallow* 복사는 새로운 개체를 생성하는 대신 캡슐화된 `BSTR` 개체의 참조 수를 증가시킵니다.|  
|`_bstr_t( char*`  `s2`  `)`|새 `BSTR` 개체를 만드는 `SysAllocString`을 호출하여 `_bstr_t` 개체를 생성한 다음 캡슐화합니다.<br /><br /> 이 생성자는 먼저 멀티바이트를 유니코드로 변환합니다.|  
|`_bstr_t( wchar_t*`  `s3`  `)`|새 `BSTR` 개체를 만드는 `SysAllocString`을 호출하여 `_bstr_t` 개체를 생성한 다음 캡슐화합니다.|  
|`_bstr_t( _variant_t&`  `var`  `)`|캡슐화된 VARIANT 개체에서 `BSTR` 개체를 먼저 검색하여 `_variant_t` 개체에서 `_bstr_t` 개체를 생성합니다.|  
|`_bstr_t( BSTR`  `bstr` `, bool`  `fCopy`  `)`|기존 `BSTR`\(`wchar_t*` 문자열의 반대\)에서 `_bstr_t` 개체를 생성합니다.  `fCopy`가 false인 경우 제공된 `BSTR`은 `SysAllocString`을 사용하여 새 복사본을 만들지 않고 새 개체에 연결됩니다.<br /><br /> 이 생성자는 형식 라이브러리 헤더의 래퍼 함수에서 사용되어 인터페이스 메서드에서 반환하는 `BSTR`을 캡슐화하고 그 소유권을 가집니다.|  
  
 **Microsoft 전용 종료**  
  
## 참고 항목  
 [\_bstr\_t 클래스](../cpp/bstr-t-class.md)   
 [\_variant\_t 클래스](../cpp/variant-t-class.md)