---
title: "숫자, 부울 및 포인터 리터럴(C++) | Microsoft Docs"
ms.custom: ""
ms.date: "12/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "language-reference"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "상수, 리터럴"
  - "리터럴"
  - "리터럴, C++"
ms.assetid: 17c09fc3-3ad7-47e2-8b48-ba8ae994edc8
caps.latest.revision: 16
caps.handback.revision: 16
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
---
# 숫자, 부울 및 포인터 리터럴(C++)
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

리터럴은 값을 직접 나타내는 프로그램 요소입니다.  이 문서에서는 정수, 부동 소수점, 부울 및 포인터 형식의 리터럴에 대해 설명합니다.  문자열 및 문자 리터럴에 대한 자세한 내용은 [문자열 및 문자 리터럴\(C\+\+\)](../cpp/string-and-character-literals-cpp.md)을 참조하세요.  이러한 범주에 따라 고유한 리터럴을 정의할 수도 있습니다. 자세한 내용은 [사용자 정의 리터럴\(C\+\+\)](../cpp/user-defined-literals-cpp.md)을 참조하세요  
  
 입니다.  리터럴은 많은 컨텍스트에서 사용할 수 있지만 가장 일반적으로 명명된 변수를 초기화하고 인수를 함수에 전달하는 데 사용됩니다.  
  
```  
const int answer = 42; // integer literal  
double d = sin(108.87);     //floating point literal passed to sin function  
bool b = true;              // boolean literal  
MyClass* mc = nullptr;      // pointer literal  
  
```  
  
 경우에 따라 리터럴을 해석하는 방법 또는 지정할 특정 형식을 컴파일러에 알려야 합니다.  이렇게 하려면 리터럴에 접두사나 접미사를 추가합니다.  예를 들어 접두사 0x는 해당 접두사 뒤에 오는 숫자를 16진수 값\(예: 0x35\)으로 해석하도록 컴파일러에 알립니다.  ULL 접미사는 5894345ULL에서처럼 값을 `unsigned long long` 형식으로 처리하도록 컴파일러에 알립니다.  각 리터럴 형식에 대한 접두사 및 접미사의 전체 목록을 다음 섹션을 참조하세요.  
  
## 구문  
  
## 정수 리터럴  
 정수 리터럴은 숫자로 시작하고 소수 부분이나 지수가 없습니다.  정수 리터럴은 10진수, 8진수 또는 16진수 형식으로 지정할 수 있습니다.  부호가 있는 또는 부호가 없는 형식 및 long 또는 short 형식을 지정할 수 있습니다.  
  
 접두사나 접미사가 없는 경우 값이 적합하면 컴파일러는 정수 리터럴 값 형식 `int`\(32비트\)를 지정하고, 그렇지 않으면 `long long` 형식\(64비트\)을 지정합니다.  
  
 10진수 정수 계열 리터럴을 지정하려면 0이 아닌 숫자를 사용하여 지정을 시작합니다.  예를 들면 다음과 같습니다.  
  
```  
int i = 157;   // Decimal literal  
int j = 0198;       // Not a decimal number; erroneous octal literal  
int k = 0365;       // Leading zero specifies octal literal, not decimal  
int m = 36'000'000  // digit separators make large values more readable  
int   
```  
  
 8진수 정수 계열 리터럴을 지정하려면 0으로 시작하여 0부터 7까지의 숫자 시퀀스를 지정합니다.  8진수 리터럴을 지정할 때 숫자 8과 9는 오류입니다.  예를 들면 다음과 같습니다.  
  
```  
int i = 0377;   // Octal literal  
int j = 0397;        // Error: 9 is not an octal digit  
```  
  
 16진수 정수 계열 리터럴을 지정하려면 `0x` 또는 `0X`\("x"의 대\/소문자 구분 안 함\)로 시작하여 `0`부터 `9` 및 `a`\(또는 `A`\)부터 `f`\(또는 `F`\)의 숫자 시퀀스를 지정합니다.  16진수 숫자 `a`\(또는 `A`\)부터 `f`\(또는 `F`\)는 10부터 15 사이의 값을 나타냅니다.  예를 들면 다음과 같습니다.  
  
```  
int i = 0x3fff;   // Hexadecimal literal  
int j = 0X3FFF;        // Equal to i  
```  
  
 부호 없는 데이터 형식을 지정하려면 **u** 또는 **U** 접미사를 사용합니다.  long 형식을 지정하려면 **l** 또는 **L** 접미사를 사용합니다.  64비트 정수 계열 형식을 지정하려면 LL 또는 ll 접미사를 사용합니다.  i64 접미사는 계속 지원되지만 Microsoft 전용이고 이식할 수 없으므로 사용하지 않아야 합니다.  예를 들면 다음과 같습니다.  
  
```  
unsigned val_1 = 328u;             // Unsigned value  
long val_2 = 0x7FFFFFL;                 // Long value specified   
                                        //  as hex literal  
unsigned long val_3 = 0776745ul;        // Unsigned long value  
auto val_4 = 108LL;                           // signed long long  
auto val_4 = 0x8000000000000000ULL << 16;     // unsigned long long   
```  
  
 **자릿수 구분 기호**: 큰 수의 자리 값을 작은따옴표\(아포스트로피\)로 구분하여 읽기 쉽게 만들 수 있습니다.  구분 기호는 컴파일에 영향을 주지 않습니다.  
  
```  
long long i = 24'847'458'121  
```  
  
## 부동 소수점 리터럴  
 부동 소수점 리터럴은 소수 부분이 있어야 하는 값을 지정합니다.  이러한 값은 소수점\(**.**\)을 포함하며 지수를 포함할 수 있습니다.  
  
 부동 소수점 리터럴에는 숫자의 값을 지정하는 "가수", 숫자의 크기를 지정하는 "지수" 및 리터럴의 형식을 지정하는 선택적 접미사가 있습니다.  가수는 숫자 시퀀스 및 그 뒤의 점과 숫자의 소수 부분을 나타내는 그 뒤의 선택적 숫자 시퀀스로 지정됩니다.  예를 들면 다음과 같습니다.  
  
```  
18.46  
38.  
```  
  
 지수는\(있는 경우\) 다음 예제와 같이 숫자의 크기를 10의 거듭제곱으로 지정합니다.  
  
```  
18.46e0      // 18.46  
18.46e1           // 184.6  
```  
  
 지수는 의미가 동일한 **e** 또는 **E**와 그 뒤에 선택적 부호\(\+ 또는 \-\) 및 숫자 시퀀스를 사용하여 지정할 수 있습니다.  지수가 있는 경우 `18E0`과 같은 정수에는 뒤에 오는 소수점이 필요하지 않습니다.  
  
 부동 소수점 리터럴은 기본적으로 **double** 형식입니다.  접미사 **f** 또는 **l**\(또는 **F** 또는 **L** \- 접미사는 대\/소문자를 구분하지 않음\)을 사용하여 리터럴을 각각 **float** 또는 `long double`로 지정할 수 있습니다.  
  
 `long double` 및 **double**은 표현은 동일하지만 같은 형식이 아닙니다.  예를 들어 다음과 같은 오버로드된 함수를 사용할 수 있습니다.  
  
```  
void func( double );  
```  
  
 및  
  
```  
void func( long double );  
```  
  
## 부울 리터럴  
 부울 리터럴은 `true` 및 `false`입니다.  
  
## 포인터 리터럴\(C\+\+11\)  
 C\+\+에서는 [nullptr](../cpp/nullptr.md) 리터럴을 사용하여 0으로 초기화된 포인터를 지정합니다.  이식 가능한 코드에서 `nullptr`은 NULL과 같이 정수 계열 형식의 0 또는 매크로 대신 사용해야 합니다.  
  
## 이진 리터럴\(C\+\+14\)  
 이진 리터럴은 `0B` 또는 `0b` 접두사와 뒤에 오는 1과 0의 시퀀스를 사용하여 지정할 수 있습니다.  
  
```  
  
auto x = 0B001101 ; // int  
auto y = 0b000001 ; // int  
```  
  
## 리터럴을 "매직 상수”로 사용하지 마세요.  
 리터럴은 식과 문에서 직접 사용할 수 있지만 항상 바람직한 프로그래밍 방법은 아닙니다.  
  
```  
if (num < 100)  
    return "Success";  
  
```  
  
 이전 예제에서는 명확한 의미를 전달하는 명명된 상수\(예: "MAXIMUM\_ERROR\_THRESHOLD"\)를 사용하는 것이 더 나을 수 있습니다.  또한 최종 사용자에게 "성공"이라는 반환 값이 표시되는 경우 다른 언어로 지역화할 수 있는 파일의 단일 위치에 저장할 수 있는 명명된 문자열 상수를 사용하는 것이 더 좋을 수 있습니다.  명명된 상수를 사용하면 모든 사람이 코드의 의도를 쉽게 파악할 수 있습니다.  
  
## 참고 항목  
 [어휘 규칙](../cpp/lexical-conventions.md)   
 [C\+\+ 정수 상수](http://msdn.microsoft.com/ko-kr/1f3b58a4-8346-4533-ba6e-df26d76f8dcf)   
 [C\+\+ 문자 리터럴](http://msdn.microsoft.com/ko-kr/a7901c61-524d-47c6-beb6-d9dacc2e72ed)   
 [C\+\+ 부동 소수점 상수](http://msdn.microsoft.com/ko-kr/f6273f24-a876-4484-a7a2-e82275692ad3)   
 [C\+\+ 문자열 리터럴](../cpp/string-and-character-literals-cpp.md)   
 [C\+\+ 사용자 정의 리터럴](../cpp/user-defined-literals-cpp.md)