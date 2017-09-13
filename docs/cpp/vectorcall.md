---
title: "__vectorcall | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "language-reference"
dev_langs: 
  - "C++"
ms.assetid: 1c95ed59-86c6-4857-b4ed-10519193f851
caps.latest.revision: 11
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 11
---
# __vectorcall
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

**Microsoft 전용**  
  
 `__vectorcall` 호출 규칙은 가능하면 함수의 인수가 레지스터에 전달되도록 지정합니다.  `__vectorcall`은 [\_\_fastcall](../cpp/fastcall.md) 또는 기본 [x64 호출 규칙](../build/overview-of-x64-calling-conventions.md)보다 인수에 레지스터를 더 많이 사용하도록 합니다.  `__vectorcall` 호출 규칙은 SSE2\(스트리밍 SIMD 확장 2\) 이상을 포함하는 x86 및 x64 프로세서의 네이티브 코드에서만 지원됩니다.  `__vectorcall`을 사용하여 여러 부동 소수점 또는 SIMD 벡터 인수를 전달하는 함수의 속도를 높이고 레지스터에 로드된 인수를 활용하는 작업을 수행합니다.  다음 목록은 `__vectorcall`을 x86 및 x64에서 구현할 때 공통적으로 사용되는 기능을 보여 줍니다.  차이점은 이 문서의 뒷부분에 설명되어 있습니다.  
  
|요소|구현|  
|--------|--------|  
|C 이름 데코레이션 규칙|함수 이름은 두 개의 "at" 기호\(@@\)가 접미사로 붙고 그 뒤에 매개 변수 목록의 바이트 수\(10진수\)가 이어집니다.|  
|대\/소문자 변환 규칙|대\/소문자 변환은 수행되지 않습니다.|  
  
 [\/Gv](../build/reference/gd-gr-gv-gz-calling-convention.md) 컴파일러 옵션을 사용하면 모듈의 각 함수를 `__vectorcall`로 컴파일합니다. 이때 함수는 멤버 함수이거나 충돌하는 호출 규칙 특성으로 선언되거나 `vararg` 변수 인수 목록을 사용하거나 이름이 `main`인 경우가 아니어야 합니다.  
  
 `__vectorcall` 함수에 등록하여 다음 세 가지 인수 *정수 형식* 값, *벡터 형식* 값 및 HVA*\(균질 벡터 집합체\)* 값을 전달할 수 있습니다.  
  
 정수 형식은 프로세서의 네이티브 레지스터 크기에 적합하며\(예: x86 컴퓨터에서는 4바이트 또는 x64 컴퓨터에서는 8바이트\) 레지스터 길이의 정수로 변환한 후 비트 표현을 변경하지 않고 다시 변환하는 두 요구 사항을 충족합니다.  예를 들어, x86의 `int`\(x64에서는 `long long`\)로 승격할 수 있는 형식\(예: `char` 또는 `short`\) 또는 `int`\(x64에서는 `long long`\)로 캐스팅되고 변경 없이 원래 형식으로 되돌릴 수 있는 형식은 정수 형식입니다.  정수 형식은 4바이트\(x64에서는 8바이트\) 이하의 포인터, 참조 및 `struct` 또는 `union` 형식을 포함합니다.  x64 플랫폼에서 큰 `struct` 및 `union` 형식은 호출자에 의해 할당된 메모리에 대한 참조에 의해 전달됩니다. x86 플랫폼에서는 스택 값에 의해 전달됩니다.  
  
 벡터 형식은 부동 소수점 형식\(예: `float` 또는 `double`\) 또는 SIMD 벡터 형식\(예: `__m128` 또는 `__m256`\) 중 하나입니다.  
  
 HVA 형식은 동일한 벡터 형식을 갖는 최대 4개의 데이터 멤버로 구성된 복합 형식입니다.  HVA 형식은 멤버의 벡터 형식과 맞춤 요구 사항이 동일합니다.  다음은 세 가지 동일한 벡터 형식과 32바이트 맞춤을 보여 주는 HVA `struct` 정의에 대한 예제입니다.  
  
```cpp  
typedef struct {  
   __m256 x;  
   __m256 y;  
   __m256 z;  
} hva3;    // 3 element HVA type on __m256  
  
```  
  
 헤더 파일에 있는 `__vectorcall` 키워드를 사용하여 명시적으로 함수를 선언하여 오류 없이 링크에 별도로 컴파일된 코드를 허용합니다.  함수는 `__vectorcall`을 사용할 수 있도록 프로토타입화되어야 하며 `vararg` 변수 길이 인수 목록을 사용할 수 없습니다.  
  
 `__vectorcall` 지정자를 사용하여 멤버 함수를 선언할 수 있습니다.  숨겨진 `this` 포인터는 첫 번째 정수 형식 인수 레지스터에 의해 전달됩니다.  
  
 ARM 컴퓨터에서는 컴파일러가 `__vectorcall`을 수락할지 무시할지 결정합니다.  
  
 비정적 클래스 멤버 함수의 경우 함수가 아웃오브 라인으로 정의되면 호출 규칙 한정자를 아웃오브 라인 정의에서 지정하지 않아도 됩니다.  즉, 클래스 비정적 멤버의 경우 선언하는 동안 지정된 호출 규칙이 정의 시에 가정됩니다.  다음의 클래스 정의를 가정해 봅니다.  
  
```cpp  
struct MyClass {  
   void __vectorcall mymethod();  
};  
```  
  
 다음 코드는  
  
```cpp  
void MyClass::mymethod() { return; }  
```  
  
 다음 코드 조각과 일치합니다.  
  
```cpp  
void __vectorcall MyClass::mymethod() { return; }  
```  
  
 `__vectorcall` 호출 규칙 한정자는 `__vectorcall` 함수에 대한 포인터가 만들어진 경우 지정되어야 합니다.  다음 예제는 4개의 `double` 인수를 사용하며 `__m256` 값을 반환하는 `__vectorcall` 함수 포인터의 `typedef`를 만듭니다.  
  
```cpp  
typedef __m256 (__vectorcall * vcfnptr)(double, double, double, double);  
```  
  
## x64의 \_\_vectorcall 규칙  
 x64의 `__vectorcall` 호출 규칙은 표준 x64 호출 규칙을 확장하여 추가 레지스터를 활용합니다.  정수 형식 인수와 벡터 형식 인수 모두 인수 목록에 있는 위치를 기반으로 레지스터에 매핑됩니다.  HVA 인수는 사용되지 않는 벡터 레지스터에 할당됩니다.  
  
 왼쪽에서 오른쪽 순서로 처음 네 개의 인수가 정수 형식 인수인 경우 해당 위치 RCX, RDX, R8 또는 R9에 해당하는 레지스터에서 전달됩니다.  숨겨진 `this` 포인터는 첫 번째 정수 형식 인수로 처리됩니다.  처음 네 개의 인수 중 하나에 있는 HVA 인수를 사용 가능한 레지스터에서 전달할 수 없을 경우, 그 대신 호출자가 할당한 메모리에 대한 참조를 해당 정수 형식 레지스터에서 전달합니다.  네 번째 매개 변수 위치 뒤에 오는 정수 형식 인수는 스택에서 전달됩니다.  
  
 왼쪽에서 오른쪽 순서로 처음 여섯 개의 인수가 벡터 형식 인수인 경우 인수 위치에 따라 0에서 5의 SSE 벡터 레지스터 값에 의해 전달됩니다.  부동 소수점 및 `__m128` 형식은 XMM 레지스터에서 전달되고 `__m256` 형식은 YMM 레지스터에서 전달됩니다.  벡터 형식이 참조가 아닌 값에 의해 전달되고 추가 레지스터가 사용되므로 이는 표준 x64 호출 규칙과 다릅니다.  벡터 형식 인수에 할당된 섀도 스택 공간은 8바이트로 고정되어 있으며 [\/homeparams](../build/reference/homeparams-copy-register-parameters-to-stack.md) 옵션이 적용되지 않습니다.  일곱 번째 이후의 매개 변수 자리에 오는 벡터 형식 인수는 호출자가 할당한 메모리에 대한 참조에 의해 스택에서 전달됩니다.  
  
 벡터 인수가 레지스터에 할당된 후 HVA 인수의 데이터 멤버는 전체 HVA에 사용할 수 있는 레지스터가 충분하지 않는 한 사용되지 않은 벡터 레지스터 XMM0~XMM5\(`__m256` 형식인 경우 YMM0~YMM5\)에 오름차순으로 할당됩니다.  사용할 수 있는 레지스터가 충분하지 않은 경우 HVA 인수는 호출자가 할당한 메모리에 대한 참조에 의해 전달됩니다.  HVA 인수에 대한 스택 섀도 공간은 정의되지 않은 내용을 포함하여 8바이트로 고정됩니다.  HVA 인수는 매개 변수 목록의 왼쪽에서 오른쪽 순서로 레지스터에 할당되며 어떤 위치에나 있을 수 있습니다.  벡터 레지스터에 할당되지 않은 처음 네 개의 인수 위치 중 하나에 있는 HVA 인수는 해당 위치에 대응하는 정수 레지스터에서 참조에 의해 전달됩니다.  네 번째 매개 변수 위치 뒤로 참조에 의해 전달된 HVA 인수는 스택에서 푸시됩니다.  
  
 `__vectorcall` 함수의 결과는 가능한 경우 레지스터에 값으로 반환됩니다.  8바이트 이하의 정수 형식 구조체 또는 공용 구조체를 포함한 정수 형식의 결과는 RAX에 값으로 반환됩니다.  벡터 형식 결과는 크기에 따라 XMM0 또는 YMM0에 값으로 반환됩니다.  HVA 결과에는 요소 크기에 따라 레지스터 XMM0:XMM3 또는 YMM0:YMM3에 값으로 반환되는 각 데이터 요소가 있습니다.  해당 레지스터에 맞지 않는 결과 형식은 호출자가 할당한 메모리에 대한 참조로 반환됩니다.  
  
 `__vectorcall`의 x64 구현에서는 호출자가 스택을 유지 관리합니다.  호출자 프롤로그 및 에필로그 코드는 호출된 함수의 스택을 할당하고 호출합니다.  인수는 오른쪽에서 왼쪽으로 스택에서 푸시되며 섀도 스택 공간에는 레지스터에 의해 전달된 인수가 할당됩니다.  
  
 예를 들면 다음과 같습니다.  
  
```cpp  
// crt_vc64.c  
// Build for amd64 with: cl /arch:AVX /W3 /FAs crt_vc64.c  
// This example creates an annotated assembly listing in  
// crt_vc64.asm.  
  
#include <intrin.h>  
#include <xmmintrin.h>  
  
typedef struct {  
   __m128 array[2];  
} hva2;    // 2 element HVA type on __m128  
  
typedef struct {  
   __m256 array[4];  
} hva4;    // 4 element HVA type on __m256  
  
// Example 1: All vectors  
// Passes a in XMM0, b in XMM1, c in YMM2, d in XMM3, e in YMM4.  
// Return value in XMM0.  
__m128 __vectorcall   
example1(__m128 a, __m128 b, __m256 c, __m128 d, __m256 e) {  
   return d;  
}  
  
// Example 2: Mixed int, float and vector parameters  
// Passes a in RCX, b in XMM1, c in R8, d in XMM3, e in YMM4,   
// f in XMM5, g pushed on stack.   
// Return value in YMM0.  
__m256 __vectorcall   
example2(int a, __m128 b, int c, __m128 d, __m256 e, float f, int g) {  
   return e;  
}  
  
// Example 3: Mixed int and HVA parameters  
// Passes a in RCX, c in R8, d in R9, and e pushed on stack.  
// Passes b by element in [XMM0:XMM1];   
// b's stack shadow area is 8-bytes of undefined value.   
// Return value in XMM0.  
__m128 __vectorcall example3(int a, hva2 b, int c, int d, int e) {  
   return b.array[0];  
}  
  
// Example 4: Discontiguous HVA   
// Passes a in RCX, b in XMM1, d in XMM3, and e is pushed on stack.  
// Passes c by element in [YMM0,YMM2,YMM4,YMM5], discontiguous because  
// vector arguments b and d were allocated first.   
// Shadow area for c is an 8-byte undefined value.  
// Return value in XMM0.  
float __vectorcall example4(int a, float b, hva4 c, __m128 d, int e) {  
   return b;  
}  
  
// Example 5: Multiple HVA arguments  
// Passes a in RCX, c in R8, e pushed on stack.  
// Passes b in [XMM0:XMM1], d in [YMM2:YMM5], each with   
// stack shadow areas of an 8-byte undefined value.  
// Return value in RAX.  
int __vectorcall example5(int a, hva2 b, int c, hva4 d, int e) {  
   return c + e;  
}  
  
// Example 6: HVA argument passed by reference, returned by register  
// Passes a in [XMM0:XMM1], b passed by reference in RDX, c in YMM2,   
// d in [XMM3:XMM4].   
// Register space was insufficient for b, but not for d.  
// Return value in [YMM0:YMM3].  
hva4 __vectorcall example6(hva2 a, hva4 b, __m256 c, hva2 d) {  
   return b;  
}  
  
int __cdecl main( void )  
{  
   hva4 h4;  
   hva2 h2;  
   int i;  
   float f;  
   __m128 a, b, d;  
   __m256 c, e;  
  
   a = b = d = _mm_set1_ps(3.0f);  
   c = e = _mm256_set1_ps(5.0f);  
   h2.array[0] = _mm_set1_ps(6.0f);  
   h4.array[0] = _mm256_set1_ps(7.0f);  
  
   b = example1(a, b, c, d, e);  
   e = example2(1, b, 3, d, e, 6.0f, 7);  
   d = example3(1, h2, 3, 4, 5);  
   f = example4(1, 2.0f, h4, d, 5);  
   i = example5(1, h2, 3, h4, 5);  
   h4 = example6(h2, h4, c, h2);  
}  
  
```  
  
## x86의 \_\_vectorcall 규칙  
 `__vectorcall` 호출 규칙은 32비트 정수 형식 인수에 `__fastcall` 규칙을 적용하며 벡터 형식 및 HVA 인수에는 SSE 벡터 레지스터를 활용합니다.  
  
 매개 변수 목록에서 왼쪽에서 오른쪽 순서로 처음 두 개 정수 형식 인수는 각각 ECX 및 EDX에 배치됩니다.  숨겨진 `this` 포인터는 첫 번째 정수 형식 인수로 처리되고 ECX에서 전달됩니다.  처음 여섯 개 벡터 형식 인수는 인수 크기에 따라 0에서 5의 SSE 벡터 레지스터 값에 의해 XMM 또는 YMM 레지스터에서 전달됩니다.  
  
 왼쪽에서 오른쪽 순서로 처음 여섯 개 벡터 형식 인수는 0에서 5의 SSE 벡터 레지스터 값에 의해 전달됩니다.  부동 소수점 및 `__m128` 형식은 XMM 레지스터에서 전달되고 `__m256` 형식은 YMM 레지스터에서 전달됩니다.  레지스터에 의해 전달된 벡터 형식 인수에는 섀도 스택 공간이 할당되지 않습니다.  일곱 번째 이후의 벡터 형식 인수는 호출자가 할당한 메모리에 대한 참조에 의해 스택에서 전달됩니다.  이 인수에는 컴파일러 오류 [C2719](../error-messages/compiler-errors-2/compiler-error-c2719.md) 제한이 적용되지 않습니다.  
  
 벡터 인수가 레지스터에 할당된 후 HVA 인수의 데이터 멤버는 전체 HVA에 사용할 수 있는 레지스터가 충분하지 않는 한 사용되지 않은 벡터 레지스터 XMM0~XMM5\(`__m256` 형식인 경우 YMM0~YMM5\)에 오름차순으로 할당됩니다.  사용할 수 있는 레지스터가 충분하지 않은 경우 HVA 인수는 호출자가 할당한 메모리에 대한 참조에 의해 스택에서 전달됩니다.  HVA 인수에는 스택 섀도 공간이 할당되지 않습니다.  HVA 인수는 매개 변수 목록의 왼쪽에서 오른쪽 순서로 레지스터에 할당되며 어떤 위치에나 있을 수 있습니다.  
  
 `__vectorcall` 함수의 결과는 가능한 경우 레지스터에 값으로 반환됩니다.  4바이트 이하의 정수 형식 구조체 또는 공용 구조체를 포함한 정수 형식의 결과는 EAX에 값으로 반환됩니다.  8바이트 이하의 정수 형식 구조체 또는 공용 구조체는 EDX:EAX에 값으로 반환됩니다.  벡터 형식 결과는 크기에 따라 XMM0 또는 YMM0에 값으로 반환됩니다.  HVA 결과에는 요소 크기에 따라 레지스터 XMM0:XMM3 또는 YMM0:YMM3에 값으로 반환되는 각 데이터 요소가 있습니다.  다른 결과 형식은 호출자가 할당한 메모리에 대한 참조로 반환됩니다.  
  
 `__vectorcall`의 x86 구현은 호출자가 오른쪽에서 왼쪽으로 스택에 푸시한 인수 규칙을 따르며 호출된 함수는 반환되기 전에 스택을 지웁니다.  레지스터에 배치되지 않은 인수만 스택으로 푸시됩니다.  
  
 예를 들면 다음과 같습니다.  
  
```cpp  
// crt_vc86.c  
// Build for x86 with: cl /arch:AVX /W3 /FAs crt_vc86.c  
// This example creates an annotated assembly listing in  
// crt_vc86.asm.  
  
#include <intrin.h>  
#include <xmmintrin.h>  
  
typedef struct {  
   __m128 array[2];  
} hva2;    // 2 element HVA type on __m128  
  
typedef struct {  
   __m256 array[4];  
} hva4;    // 4 element HVA type on __m256  
  
// Example 1: All vectors  
// Passes a in XMM0, b in XMM1, c in YMM2, d in XMM3, e in YMM4.  
// Return value in XMM0.  
__m128 __vectorcall   
example1(__m128 a, __m128 b, __m256 c, __m128 d, __m256 e) {  
   return d;  
}  
  
// Example 2: Mixed int, float and vector parameters  
// Passes a in ECX, b in XMM0, c in EDX, d in XMM1, e in YMM2,   
// f in XMM3, g pushed on stack.   
// Return value in YMM0.  
__m256 __vectorcall   
example2(int a, __m128 b, int c, __m128 d, __m256 e, float f, int g) {  
   return e;  
}  
  
// Example 3: Mixed int and HVA parameters  
// Passes a in ECX, c in EDX, d and e pushed on stack.  
// Passes b by element in [XMM0:XMM1].   
// Return value in XMM0.  
__m128 __vectorcall example3(int a, hva2 b, int c, int d, int e) {  
   return b.array[0];  
}  
  
// Example 4: HVA assigned after vector types  
// Passes a in ECX, b in XMM0, d in XMM1, and e in EDX.  
// Passes c by element in [YMM2:YMM5].   
// Return value in XMM0.  
float __vectorcall example4(int a, float b, hva4 c, __m128 d, int e) {  
   return b;  
}  
  
// Example 5: Multiple HVA arguments  
// Passes a in ECX, c in EDX, e pushed on stack.  
// Passes b in [XMM0:XMM1], d in [YMM2:YMM5].  
// Return value in EAX.  
int __vectorcall example5(int a, hva2 b, int c, hva4 d, int e) {  
   return c + e;  
}  
  
// Example 6: HVA argument passed by reference, returned by register  
// Passes a in [XMM1:XMM2], b passed by reference in ECX, c in YMM0,   
// d in [XMM3:XMM4].   
// Register space was insufficient for b, but not for d.  
// Return value in [YMM0:YMM3].  
hva4 __vectorcall example6(hva2 a, hva4 b, __m256 c, hva2 d) {  
   return b;  
}  
  
int __cdecl main( void )  
{  
   hva4 h4;  
   hva2 h2;  
   int i;  
   float f;  
   __m128 a, b, d;  
   __m256 c, e;  
  
   a = b = d = _mm_set1_ps(3.0f);  
   c = e = _mm256_set1_ps(5.0f);  
   h2.array[0] = _mm_set1_ps(6.0f);  
   h4.array[0] = _mm256_set1_ps(7.0f);  
  
   b = example1(a, b, c, d, e);  
   e = example2(1, b, 3, d, e, 6.0f, 7);  
   d = example3(1, h2, 3, 4, 5);  
   f = example4(1, 2.0f, h4, d, 5);  
   i = example5(1, h2, 3, h4, 5);  
   h4 = example6(h2, h4, c, h2);  
}  
  
```  
  
 **Microsoft 전용 종료**  
  
## 참고 항목  
 [인수 전달 및 명명 규칙](../cpp/argument-passing-and-naming-conventions.md)   
 [C\+\+ 키워드](../cpp/keywords-cpp.md)