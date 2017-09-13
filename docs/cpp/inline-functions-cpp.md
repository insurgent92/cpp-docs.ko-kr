---
title: "인라인 함수(C++) | Microsoft Docs"
ms.custom: ""
ms.date: "12/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "language-reference"
f1_keywords: 
  - "__forceinline_cpp"
  - "__inline_cpp"
  - "inline_cpp"
  - "__forceinline"
  - "__inline"
  - "inline"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "인라인 함수, 클래스 멤버"
ms.assetid: 355f120c-2847-4608-ac04-8dda18ffe10c
caps.latest.revision: 11
caps.handback.revision: 9
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
---
# 인라인 함수(C++)
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

클래스 선언의 본문에 정의된 함수는 인라인 함수입니다.  
  
## 예제  
 다음 클래스 선언에서 `Account` 생성자는 인라인 함수입니다.  멤버 함수인 `GetBalance`, `Deposit` 및 `Withdraw`는 **inline**으로 지정되지 않았지만 인라인 함수로 구현할 수 있습니다.  
  
```  
// Inline_Member_Functions.cpp  
class Account  
{  
public:  
    Account(double initial_balance) { balance = initial_balance; }  
    double GetBalance();  
    double Deposit( double Amount );  
    double Withdraw( double Amount );  
private:  
    double balance;  
};  
  
inline double Account::GetBalance()  
{  
    return balance;  
}  
  
inline double Account::Deposit( double Amount )  
{  
    return ( balance += Amount );  
}  
  
inline double Account::Withdraw( double Amount )  
{  
    return ( balance -= Amount );  
}  
int main()  
{  
}  
```  
  
> [!NOTE]
>  클래스 선언에서 함수가 **inline** 키워드 없이 선언되었습니다.  **inline** 키워드는 클래스 선언에서 지정할 수 있으며 결과는 동일합니다.  
  
 주어진 인라인 멤버 함수는 모든 컴파일 단위에서 동일한 방식으로 선언되어야 합니다.  이 제한 사항으로 인해 인라인 함수는 마치 인스턴스화된 함수처럼 동작합니다.  또한 인라인 함수의 정의는 정확히 하나만 있어야 합니다.  
  
 클래스 멤버 함수는 해당 함수에 대한 정의에 **inline** 지정자가 포함되지 않으면 외부 링크를 기본적으로 가집니다.  앞의 예제는 이들 함수가 **inline** 지정자를 사용하여 명시적으로 선언될 필요가 없음을 보여 줍니다. 함수 정의에서 **inline**을 사용하면 인라인 함수가 됩니다.  하지만 함수 호출 후에 해당 함수를 **inline**으로 다시 선언하는 것은 올바르지 않습니다.  
  
## Inline, \_\_inline 및 \_\_forceinline  
 `inline` 및 `__inline` 지정자는 함수 본문의 복사본을 함수가 호출되는 각 위치에 삽입하도록 컴파일러에 지시합니다.  
  
 삽입\(인라인 확장 또는 인라인 처리라고 함\)은 컴파일러의 비용\/이익 분석에서 수익성이 있는 것으로 표시되는 경우에만 수행됩니다.  인라인 확장을 사용하면 더 큰 코드 크기를 줄여 함수 호출 오버헤드를 줄일 수 있습니다.  
  
 `__forceinline` 키워드는 비용\/이익 분석을 재정의하고 대신 프로그래머의 판단에 의존합니다.  `__forceinline`을 사용할 때는 주의해야 합니다.  `__forceinline`을 무분별하게 사용하면 코드가 더 커져 성능이 크게 향상되지 않거나, 경우에 따라 더 큰 실행 파일의 페이징 증가와 같은 이유로 성능이 손실될 수도 있습니다.  
  
 인라인 함수를 사용하면 함수 호출과 연관된 오버헤드가 제거되어 프로그램 속도가 더 빨라질 수 있습니다.  인라인으로 확장된 함수에는 일반 함수에 사용할 수 없는 코드 최적화가 적용됩니다.  
  
 컴파일러는 인라인 확장 옵션과 키워드를 제안으로 처리합니다.  함수가 인라인으로 처리된다는 보장은 없습니다.  `__forceinline` 키워드를 사용해도 컴파일러에서 특정 함수를 강제로 인라인 처리하도록 할 수는 없습니다.  **\/clr**로 컴파일할 때 컴파일러는 함수에 적용된 보안 특성이 있으면 함수를 인라인 처리하지 않습니다.  
  
 **inline** 키워드는 C\+\+에서만 사용할 수 있습니다.  `__inline` 및 `__forceinline` 키워드는 C와 C\+\+ 둘 다에서 사용할 수 있습니다.  이전 버전과의 호환성을 위해 **\_inline**은 `__inline`의 동의어입니다.  
  
 **inline** 키워드는 인라인 확장이 더 적합함을 컴파일러에 알립니다.  그러나 컴파일러는 함수의 별도 인스턴스를 만들고\(인스턴스화\) 인라인으로 코드를 삽입하는 대신 표준 호출 링크를 만들 수 있습니다.  다음은 이런 상황이 발생할 수 있는 두 가지 경우입니다.  
  
-   재귀 함수.  
  
-   변환 단위의 다른 위치에서 포인터를 통해 참조되는 함수.  
  
 이러한 이유는 *다른 경우와 마찬가지로* 컴파일러의 판단에 따라 인라인 처리에 방해가 될 수 있습니다. 함수를 인라인 처리하려면 **inline** 지정자를 사용하지 않아야 합니다.  
  
 일반 함수에서처럼 인라인 함수에 대한 인수의 계산 순서는 정의되어 있지 않습니다.  실제로 일반 함수 호출 프로토콜을 사용하여 전달될 때 인수가 계산되는 순서와 다를 수 있습니다.  
  
 [\/Ob](../build/reference/ob-inline-function-expansion.md) 컴파일러 최적화 옵션을 사용하면 인라인 함수 확장이 실제로 발생하는지 여부를 확인할 수 있습니다.  
  
 [\/LTCG](../build/reference/ltcg-link-time-code-generation.md)는 소스 코드에서 요청되었는지 여부에 관계없이 크로스 모듈 인라인 처리를 수행합니다.  
  
### 예제 1  
  
```  
// inline_keyword1.cpp  
// compile with: /c  
inline int max( int a , int b ) {  
   if( a > b )   
      return a;  
   return b;  
}  
```  
  
 클래스의 멤버 함수는 **inline** 키워드를 사용하거나 클래스 정의 내에 함수 정의를 배치하여 인라인으로 선언할 수 있습니다.  
  
### 예제 2  
  
```  
// inline_keyword2.cpp  
// compile with: /EHsc /c  
#include <iostream>  
using namespace std;  
  
class MyClass {  
public:  
   void print() { cout << i << ' '; }   // Implicitly inline  
private:  
   int i;  
};  
```  
  
### Microsoft 전용  
 `__inline` 키워드는 **inline**과 동일합니다.  
  
 `__forceinline`을 사용해도 컴파일러가 모든 상황에서 코드를 인라인 처리할 수는 없습니다.  다음과 같은 경우 컴파일러에서 함수를 인라인 처리할 수 없습니다.  
  
-   함수 또는 해당 호출자가 \/Ob0\(디버그 빌드에 대한 기본 옵션\)으로 컴파일됩니다.  
  
-   함수 및 호출자가 다양한 형식의 예외 처리\(한 경우 C\+\+ 예외 처리, 다른 경우 구조적 예외 처리\)를 사용합니다.  
  
-   함수에 가변 인수 목록이 있습니다.  
  
-   \/Og, \/Ox, \/O1 또는 \/O2로 컴파일되지 않은 경우 함수에서 인라인 어셈블리를 사용합니다.  
  
-   재귀 함수이며 **\#pragma inline\_recursion\(on\)**이 함께 지정되지 않았습니다.  pragma를 사용하면 재귀 함수가 기본 깊이 16번 호출로 인라인 처리됩니다.  인라인 처리 깊이를 줄이려면 [inline\_depth](../preprocessor/inline-depth.md) pragma를 사용합니다.  
  
-   가상 함수이며 실제로 호출됩니다.  가상 함수에 대한 직접 호출은 인라인 처리할 수 있습니다.  
  
-   프로그램에서 함수의 주소를 사용하고 함수에 대한 포인터를 통해 호출합니다.  주소가 사용된 함수에 대한 직접 호출은 인라인 처리할 수 있습니다.  
  
-   또한 함수가 [naked](../cpp/naked-cpp.md) [\_\_declspec](../cpp/declspec.md) 한정자로 표시됩니다.  
  
 컴파일러가 `__forceinline`으로 선언된 함수를 인라인 처리할 수 없으면 수준 1 경고가 생성됩니다.  
  
 재귀 함수는 [inline\_depth](../preprocessor/inline-depth.md) pragma에 지정된 깊이인 최대 16번 호출까지 인라인으로 대체할 수 있습니다.  해당 깊이 이후 재귀 함수 호출은 함수의 인스턴스 호출로 처리됩니다.  인라인 추론에서 재귀 함수를 검사하는 깊이는 16을 초과할 수 없습니다.  [inline\_recursion](../preprocessor/inline-recursion.md) pragma는 현재 확장 중인 함수의 인라인 확장을 제어합니다.  관련 정보는 [인라인 함수 확장](../build/reference/ob-inline-function-expansion.md)\(\/Ob\) 컴파일러 옵션을 참조하세요.  
  
### Microsoft 전용 종료  
 **inline** 지정자 사용에 대한 자세한 내용은 다음을 참조하세요.  
  
-   [인라인 클래스 멤버 함수](../cpp/inline-functions-cpp.md)  
  
-   [인라인 함수와 매크로 비교](../misc/inline-functions-versus-macros.md)  
  
-   [인라인 함수와 함께 사용할 때](../misc/when-to-use-inline-functions.md)  
  
-   [dllexport 및 dllimport로 인라인 C\+\+ 함수 정의](../cpp/defining-inline-cpp-functions-with-dllexport-and-dllimport.md)  
  
## 인라인 함수 사용 시기  
 인라인 함수는 전용 데이터 멤버에 액세스하는 것처럼 작은 함수에서 가장 적합하게 사용됩니다.  한 줄 또는 두 줄 "접근자" 함수의 주요 목적은 개체에 대한 상태 정보를 반환하는 것입니다. 간단한 함수는 함수 호출의 오버헤드에 민감합니다.  긴 함수는 호출\/반환 시퀀스에서 상당히 시간이 적게 소요되며 인라이닝으로 인한 이점이 크지 않습니다.  
  
 `Point`함수 호출 결과에 소개된 [클래스는 다음과 같이 최적화될 수 있습니다.](../misc/function-call-results.md)  
  
```  
// when_to_use_inline_functions.cpp  
class Point  
{  
public:  
    // Define "accessor" functions as  
    //  reference types.  
    unsigned& x();  
    unsigned& y();  
private:  
    unsigned _x;  
    unsigned _y;  
};  
  
inline unsigned& Point::x()  
{  
    return _x;  
}  
inline unsigned& Point::y()  
{  
    return _y;  
}  
int main()  
{  
}  
```  
  
 좌표 조작이 두 접근자 함수\(앞의 예에서 `x` 및 `y`\)를 **inline**으로 지정하는 클래스의 클라이언트에서 상대적으로 일반적인 작업이라고 가정하면 일반적으로 오버헤드는 다음의 상황에서 저장됩니다.  
  
-   함수 호출\(개체의 주소를 스택에 전달 및 배치하는 매개 변수 포함\)  
  
-   호출자의 스택 프레임의 보존  
  
-   새 스택 프레임 설정  
  
-   반환 값 전달  
  
-   기존 스택 프레임 복원  
  
-   반환  
  
## 인라인 함수 및매크로  
 컴파일할 때 호출 시점에 함수 코드가 확장된다는 점에서 인라인 함수는 매크로와 비슷하지만 인라인 함수는 컴파일러에 의해 구문이 분석되며 매크로는 전처리기에 의해 확장됩니다.  그 결과 몇 가지 중요한 차이가 생깁니다.  
  
-   인라인 함수는 일반 함수에 적용되는 모든 형식 안전성 프로토콜을 따릅니다.  
  
-   인라인 함수는 함수 선언에 **inline** 키워드를 포함한다는 점을 제외하고 다른 함수와 동일한 구문을 사용하여 지정됩니다.  
  
-   인라인 함수에 인수로 전달된 식은 한 번 계산됩니다.  매크로에 인수로 전달된 식은 경우에 따라 여러 번 계산할 수 있습니다.  
  
 다음 예제에서는 소문자를 대문자로 변환하는 매크로를 보여 줍니다.  
  
```  
// inline_functions_macro.c  
#include <stdio.h>  
#include <conio.h>  
  
#define toupper(a) ((a) >= 'a' && ((a) <= 'z') ? ((a)-('a'-'A')):(a))  
  
int main() {  
   char ch;  
   printf_s("Enter a character: ");  
   ch = toupper( getc(stdin) );  
   printf_s( "%c", ch );  
}  
//  Sample Input:  xyz  
// Sample Output:  Z  
  
```  
  
 `toupper(getc(stdin))` 식의 의도는 콘솔 장치\(`stdin`\)에서 문자를 읽고 필요할 경우 대문자로 변환하는 것입니다.  
  
 매크로 구현으로 인해 문자가 "a"보다 크거나 같은지 확인하기 위해 한 번, "z"보다 작거나 같은지 확인하기 위해 한 번 `getc`를 실행합니다. 해당 범위에 속할 경우 문자를 대문자로 변환하기 위해 `getc`가 다시 실행됩니다.  즉, 문자를 1개만 기다려야 하는데 프로그램이 문자를 2개나 3개 기다립니다.  
  
 인라인 함수는 전에 설명한 문제를 해결합니다.  
  
```  
// inline_functions_inline.cpp  
#include <stdio.h>  
#include <conio.h>  
  
inline char toupper( char a ) {  
   return ((a >= 'a' && a <= 'z') ? a-('a'-'A') : a );  
}  
  
int main() {  
   printf_s("Enter a character: ");  
   char ch = toupper( getc(stdin) );  
   printf_s( "%c", ch );  
}  
```  
  
  **샘플 입력: `a`**   
 **샘플 출력: `A`**    
## 참고 항목  
 [noinline](../cpp/noinline.md)   
 [auto\_inline](../preprocessor/auto-inline.md)