---
title: "CString Operations Relating to C-Style Strings | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "reference"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "casting CString objects"
  - "CString objects, 기본 작업"
  - "C-style strings"
  - "MFC[C++], string handling class"
  - "null 값, Null-terminated string conversion"
  - "standard run-time library string functions"
  - "string arguments"
  - "문자열 변환[C++], C-style strings"
  - "문자열 함수"
  - "문자열[C++], class CString"
  - "문자열[C++], in C"
  - "문자열[C++], string operations"
ms.assetid: 5048de8a-5298-4891-b8a0-c554b5a3ac1b
caps.latest.revision: 17
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 13
---
# CString Operations Relating to C-Style Strings
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

[CString](../atl-mfc-shared/using-cstring.md) 개체는 문자열 데이터를 포함합니다.  `CString`은 문자열 데이터를 사용하도록 [CStringT](../atl-mfc-shared/reference/cstringt-class.md) 클래스 템플릿에 정의된 [메서드 및 연산자](../atl-mfc-shared/reference/cstringt-class.md) 집합을 상속합니다.  \(`CString`은 `CString`에서 지원하는 문자 데이터 종류를 사용하도록 `CStringT`를 특수화하는 `typedef`입니다.  
  
 `CString`은 문자 데이터를 C 스타일의 null로 종료되는 문자열로 저장하지 않습니다.  대신 `CString`은 필요한 데이터와 공간을 보다 안전하게 감시하기 위해 문자 데이터 길이를 추적합니다.  
  
 `CString`은 C 스타일 문자열을 허용하며 C 스타일 문자열로 문자 데이터에 액세스하는 방법을 제공합니다.  이 항목의 다음 섹션에서는 C 스타일의 null로 종료되는 문자열처럼 `CString` 개체를 사용하는 방법을 설명합니다.  
  
-   [C 스타일의 null로 종료되는 문자열로 변환](#_core_using_cstring_as_a_c.2d.style_null.2d.terminated_string)  
  
-   [표준 런타임 라이브러리 문자열 함수 사용](#_core_working_with_standard_run.2d.time_library_string_functions)  
  
-   [CString 콘텐츠 직접 수정](#_core_modifying_cstring_contents_directly)  
  
-   [가변 인수 함수와 함께 CString 개체 사용](#_core_using_cstring_objects_with_variable_argument_functions)  
  
-   [CString 정식 매개 변수 지정](#_core_specifying_cstring_formal_parameters)  
  
##  <a name="_core_using_cstring_as_a_c.2d.style_null.2d.terminated_string"></a> CString을 C 스타일의 null로 종료되는 문자열로 사용  
 `CString` 개체를 C 스타일 문자열로 사용하려면 `LPCTSTR`에 개체를 캐스팅합니다.  다음 예에서 `CString`은 C 스타일의 null로 종료되는 읽기 전용 문자열에 대한 포인터를 반환합니다.  `strcpy` 함수는 C 스타일 문자열 복사본을 `myString` 변수에 포함합니다.  
  
```  
CString aCString = "A string";  
char myString[256];  
strcpy(myString, (LPCTSTR)aCString);  
  
```  
  
 `SetAt` 등의 `CString` 메서드를 사용하여 문자열 개체에서 개별 문자를 수정할 수 있습니다.  그러나 `LPCTSTR` 포인터는 임시 항목이며 `CString`을 변경하면 무효화됩니다.  `CString`이 범위를 벗어나 자동으로 삭제될 수도 있습니다.  `CString` 개체의 `LPCTSTR` 포인터는 사용할 때마다 새로 가져오는 것이 좋습니다.  
  
 `CString` 데이터의 복사본을 직접 수정해야 할 수도 있습니다.  `CString` 개체를 별도의 버퍼에 복사하려면 보다 안전한 `strcpy_s` 함수 또는 유니코드\/MBCS 이식 가능 `_tcscpy_s`를 사용합니다.  이렇게 하면 다음 예에 나와 있는 것처럼 문자를 안전하게 수정할 수 있습니다.  
  
 [!code-cpp[NVC_ATLMFC_Utilities#189](../atl-mfc-shared/codesnippet/CPP/cstring-operations-relating-to-c-style-strings_1.cpp)]  
  
> [!NOTE]
>  `strcpy_s` 또는 유니코드\/MBCS 이식 가능 `_tcscpy_s`의 세 번째 인수는 `const``wchar_t*`\(유니코드\) 또는 `const``char*`\(ANSI\)입니다.  위의 예에서는 이 인수에 대해 `CString`을 전달합니다.  C\+\+ 컴파일러는 `CString`을 `LPCTSTR`로 변환하는 `CString` 클래스에 대해 정의된 변환 함수를 자동으로 적용합니다.  C\+\+의 가장 유용한 기능 중 하나는 형식 간의 캐스팅 작업을 정의하는 기능입니다.  
  
##  <a name="_core_working_with_standard_run.2d.time_library_string_functions"></a> 표준 런타임 라이브러리 문자열 함수 사용  
 `strcmp` 또는 유니코드\/MBCS 이식 가능 `_tcscmp`와 같은 표준 C 런타임 라이브러리 문자열 함수를 사용할 수 있는 모든 문자열 작업을 수행하는 `CString` 메서드를 찾을 수 있습니다.  
  
 C 런타임 문자열 함수를 사용해야 하는 경우 \_core\_using\_cstring\_as\_a\_c.2d.style\_null.2d.terminated\_string에서 설명하는 기술을 사용할 수 있습니다.  `CString` 개체를 해당하는 C 스타일 문자열 버퍼에 복사하고 버퍼에 대해 작업을 수행한 다음 결과로 생성된 C 스타일 문자열을 `CString` 개체에 다시 할당할 수 있습니다.  
  
##  <a name="_core_modifying_cstring_contents_directly"></a> CString 콘텐츠 직접 수정  
 대부분의 경우에는 `CString` 멤버 함수를 사용하여 `CString` 개체의 콘텐츠를 수정하거나 `CString`을 C 스타일 문자열로 변환해야 합니다.  
  
 그러나 문자 버퍼가 필요한 운영 체제 함수를 사용하는 등의 경우에는 `CString` 콘텐츠를 직접 수정할 수 있습니다.  
  
 `GetBuffer` 및 `ReleaseBuffer` 메서드를 통해 `CString` 개체의 내부 문자 버퍼에 액세스하여 해당 버퍼를 직접 수정할 수 있습니다.  다음 단계에서는 이러한 작업을 위해 해당 함수를 사용하는 방법을 보여줍니다.  
  
#### GetBuffer 및 ReleaseBuffer를 사용하여 CString 개체의 내부 문자 버퍼에 액세스하려면  
  
1.  `CString` 개체에 대해 `GetBuffer`를 호출하고 필요한 버퍼 길이를 지정합니다.  
  
2.  `GetBuffer`에서 반환하는 포인터를 사용하여 `CString` 개체에 문자를 직접 씁니다.  
  
3.  `CString` 개체에 대해 `ReleaseBuffer`를 호출하여 문자열 길이 등의 모든 내부 `CString` 상태 정보를 업데이트합니다.  `CString` 개체의 콘텐츠를 직접 수정한 후에는 `ReleaseBuffer`를 호출한 후에 다른 `CString` 멤버 함수를 호출해야 합니다.  
  
##  <a name="_core_using_cstring_objects_with_variable_argument_functions"></a> 가변 인수 함수와 함께 CString 개체 사용  
 일부 C 함수는 가변 인수 수를 사용합니다.  이러한 함수의 대표적인 예로 `printf_s`가 있습니다.  이러한 종류의 함수가 선언되는 방식으로 인해 컴파일러는 인수의 형식을 명확하게 파악할 수 없으며 각 인수에 대해 수행할 변환 작업을 결정할 수 없습니다.  따라서 가변 인수 수를 사용하는 함수로 `CString` 개체를 전달할 때는 명시적 형식 캐스팅을 사용해야 합니다.  
  
 가변 인수 함수에서 `CString` 개체를 사용하려면 다음 예에 나와 있는 것처럼 `CString`을 `LPCTSTR` 문자열에 명시적으로 캐스팅합니다.  
  
 [!code-cpp[NVC_ATLMFC_Utilities#190](../atl-mfc-shared/codesnippet/CPP/cstring-operations-relating-to-c-style-strings_2.cpp)]  
  
##  <a name="_core_specifying_cstring_formal_parameters"></a> CString 정식 매개 변수 지정  
 문자열 인수가 필요한 대부분의 함수에서는 함수 프로토타입의 정식 매개 변수를 `CString` 대신 문자에 대한 `const` 포인터\(`LPCTSTR`\)로 지정하는 것이 가장 좋습니다.  정식 매개 변수를 문자에 대한 `const` 포인터로 지정하면 `TCHAR` 배열에 대한 포인터, 리터럴 문자열 \[`"hi there"`\] 또는 `CString` 개체를 전달할 수 있습니다.  `CString` 개체는 `LPCTSTR`로 자동 변환됩니다.  `LPCTSTR`을 사용할 수 있는 모든 위치에는 `CString` 개체도 사용할 수 있습니다.  
  
 인수를 수정하지 않으려는 경우에는 정식 매개 변수를 상수 문자열 참조\(`const``CString&`\)로 지정할 수도 있습니다.  함수로 문자열을 수정하려는 경우에는 `const` 한정자를 배치합니다.  기본 null 값을 사용하려면 아래에 나와 있는 것처럼 정식 매개 변수를 null 문자열 \[`""`\]로 초기화합니다.  
  
 [!code-cpp[NVC_ATLMFC_Utilities#191](../atl-mfc-shared/codesnippet/CPP/cstring-operations-relating-to-c-style-strings_3.cpp)]  
  
 대부분의 함수 결과에 대해 값을 기준으로 `CString` 개체를 반환할 수 있습니다.  
  
## 참고 항목  
 [문자열](../atl-mfc-shared/strings-atl-mfc.md)   
 [CString Argument Passing](../atl-mfc-shared/cstring-argument-passing.md)