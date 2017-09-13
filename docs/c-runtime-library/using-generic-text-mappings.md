---
title: "일반 텍스트 매핑 사용 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- _UNICODE
dev_langs:
- C++
helpviewer_keywords:
- _TXCHAR type
- TINT type
- _TCHAR type
- TSCHAR type
- TEXT type
- TCHAR type
- TCHAR.H data types, mappings defined in
- generic-text data types
- _TINT type
- TUCHAR type
- _UNICODE constant
- TXCHAR type
- generic-text mappings
- _TSCHAR type
- T type
- mappings, generic-text
- _TUCHAR type
- MBCS data type
- _MBCS data type
- _TEXT type
- UNICODE constant
- _T type
ms.assetid: 2848121c-e51f-4b9b-a2e6-833ece4b0cb3
caps.latest.revision: 8
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
ms.translationtype: Human Translation
ms.sourcegitcommit: d6eb43b2e77b11f4c85f6cf7e563fe743d2a7093
ms.openlocfilehash: 17a3f4f7be76be9f23160e351466fee4f70b9272
ms.contentlocale: ko-kr
ms.lasthandoff: 05/18/2017

---
# <a name="using-generic-text-mappings"></a>일반 텍스트 매핑 사용
**Microsoft 전용**  
  
 Microsoft 런타임 라이브러리는 다양한 해외 시장을 겨냥하여 코드 개발을 간소화하기 위해 다양한 데이터 형식, 루틴 및 기타 개체에 대해 Microsoft 전용 "일반 텍스트" 매핑을 제공합니다. 이러한 매핑은 TCHAR.H에 정의됩니다. 이러한 이름 매핑을 사용하면 `#define` 문을 사용하여 정의하는 매니페스트 상수에 따라, 세 가지 종류의 문자 집합, 즉 ASCII(SBCS), MBCS 또는 유니코드용으로 컴파일할 수 있는 일반 코드를 쓸 수 있습니다. 제네릭 텍스트 매핑은 ANSI와 호환되지 않는 Microsoft 확장입니다.  
  
### <a name="preprocessor-directives-for-generic-text-mappings"></a>일반 텍스트 매핑용 전처리기 지시문  
  
|#define|컴파일 버전|예제|  
|--------------|----------------------|-------------|  
|`_UNICODE`|유니코드(와이드 문자)|`_tcsrev`는 `_wcsrev`에 매핑됩니다.|  
|`_MBCS`|멀티바이트 문자|`_tcsrev`는 `_mbsrev`에 매핑됩니다.|  
|없음(기본값: `_UNICODE` 및 `_MBCS` 둘 다 정의되지 않음)|SBCS(ASCII)|`_tcsrev`는 `strrev`에 매핑됩니다.|  
  
 예를 들어 TCHAR.H에 정의된 일반 텍스트 함수인 `_tcsrev`는 프로그램에 `MBCS`가 정의된 경우에는 `mbsrev`로 매핑되고, `_UNICODE`가 정의된 경우에는 `_wcsrev`로 매핑됩니다. 그렇지 않으면 `_tcsrev`는 `strrev`로 매핑됩니다.  
  
 역시 TCHAR.H에 정의된 일반 텍스트 데이터 형식 `_TCHAR`도 `_MBCS`이 정의된 경우에는 `char` 형식에 매핑되고, `_UNICODE`가 정의된 경우에는 `wchar_t` 형식으로 매핑되고, 두 상수가 모두 정의되지 않은 경우에는 `char` 형식으로 매핑됩니다. 프로그래밍 편의를 위해 다른 데이터 형식 매핑이 TCHAR.H에 제공되지만 `_TCHAR`이 가장 유용한 형식입니다.  
  
### <a name="generic-text-data-type-mappings"></a>일반 텍스트 데이터 형식 매핑  
  
|일반 텍스트 데이터 형식 이름|SBCS(_UNICODE 및 MBCS가 정의되지 않음)|_MBCS 정의됨|_UNICODE 정의됨|  
|----------------------------------|--------------------------------------------|--------------------|-----------------------|  
|`_TCHAR`|`char`|`char`|`wchar_t`|  
|`_TINT`|`int`|`int`|`wint_t`|  
|`_TSCHAR`|`signed char`|`signed char`|`wchar_t`|  
|`_TUCHAR`|`unsigned char`|`unsigned char`|`wchar_t`|  
|`_TXCHAR`|`char`|`unsigned char`|`wchar_t`|  
|`_T` 또는 `_TEXT`|효과 없음(전처리기에 의해 제거됨)|효과 없음(전처리기에 의해 제거됨)|`L`(다음 문자 또는 문자열을 유니코드 문자 또는 문자열로 변환)|  
  
 루틴, 변수 및 기타 개체의 일반 텍스트 매핑에 대한 전체 목록을 보려면 [일반 텍스트 매핑](../c-runtime-library/generic-text-mappings.md)을 참조하세요.  
  
 다음 코드 조각은 MBCS, 유니코드 및 SBCS 모델에 매핑하는 데 `_TCHAR` 및 `_tcsrev`를 사용하는 방법을 보여 줍니다.  
  
```  
_TCHAR *RetVal, *szString;  
RetVal = _tcsrev(szString);  
```  
  
 `MBCS`가 정의되면 전처리기는 위 조각을 다음 코드에 매핑합니다.  
  
```  
char *RetVal, *szString;  
RetVal = _mbsrev(szString);  
```  
  
 `_UNICODE`가 정의되면 전처리기는 같은 조각을 다음 코드에 매핑합니다.  
  
```  
wchar_t *RetVal, *szString;  
RetVal = _wcsrev(szString);  
```  
  
 `_MBCS` 또는 `_UNICODE`가 둘 다 정의되지 않은 경우 전처리기는 다음과 같이 해당 조각을 싱글바이트 ASCII 코드에 매핑합니다.  
  
```  
char *RetVal, *szString;  
RetVal = strrev(szString);  
```  
  
 따라서 이러한 세 가지 종류의 문자 집합과 관련된 루틴에서 실행할 단일 소스 코드 파일을 작성하고, 유지하고, 컴파일할 수 있습니다.  
  
 **Microsoft 전용 종료**  
  
## <a name="see-also"></a>참고 항목  
 [일반 텍스트 매핑](../c-runtime-library/generic-text-mappings.md)   
 [데이터 형식 매핑](../c-runtime-library/data-type-mappings.md)   
 [상수 및 전역 변수 매핑](../c-runtime-library/constant-and-global-variable-mappings.md)   
 [루틴 매핑](../c-runtime-library/routine-mappings.md)   
 [샘플 일반 텍스트 프로그램](../c-runtime-library/a-sample-generic-text-program.md)