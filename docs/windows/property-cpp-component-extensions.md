---
title: "property  (C++ Component Extensions) | Microsoft Docs"
ms.custom: ""
ms.date: "12/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "language-reference"
f1_keywords: 
  - "property_cpp"
  - "property"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "property keyword [C++]"
ms.assetid: cc79d2b2-f013-4d81-8252-eece97a18704
caps.latest.revision: 31
caps.handback.revision: 29
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
---
# property  (C++ Component Extensions)
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

동작하고 데이터 멤버 또는 배열 요소처럼 액세스되는 멤버 함수인 *속성*을 선언합니다.  
  
## 모든 런타임  
 다음 형식의 속성 중 하나를 선언할 수 있습니다.  
  
 *단순 속성*  
 기본적으로 속성 값을 할당하는 *set 접근자*, 속성 값을 검색하는 *get 접근자* 및 속성 값이 포함된 컴파일러에서 생성된 전용 데이터 멤버를 만듭니다.  
  
 *속성 블록*  
 사용자 정의 get 및\/또는 set 접근자를 만드는 데 사용합니다.  속성은 get 및 set 접근자를 둘 다 정의하면 읽기\/쓰기이고, get 접근자만 정의하는 읽기 전용이고, set 접근자만 정의하면 쓰기 전용입니다.  
  
 속성 값을 포함하려면 데이터 멤버를 명시적으로 선언해야 합니다.  
  
 *인덱싱된 속성*  
 하나 이상의 인덱스로 지정된 속성 값을 가져오고 설정하는 데 사용할 수 있는 속성 블록입니다.  
  
 사용자 정의 속성 이름 또는 *기본* 속성 이름이 있는 인덱싱된 속성을 만들 수 있습니다.  기본 인덱스 속성의 이름은 속성이 정의된 클래스의 이름입니다.  기본 속성을 선언하려면 속성 이름 대신 `default` 키워드를 지정합니다.  
  
 속성 값을 포함하려면 데이터 멤버를 명시적으로 선언해야 합니다.  인덱싱된 속성의 경우 데이터 멤버는 대개 배열 또는 컬렉션입니다.  
  
### 구문  
  
```cpp  
  
property type property_name;  
  
property type property_name {  
   access-modifier type get() inheritance-modifier {property_body};  
   access-modifier void set(type value) inheritance-modifier {property_body};  
} property type property_name[index_list] {  
   access-modifier type get(index_list) inheritance-modifier {property_body};  
   access-modifier void set(index_list, value) inheritance-modifier {property_body};  
} property type default[index_list] {  
   access-modifier type get(index_list) inheritance-modifier {property_body};  
   access-modifier void set(index_list, value) inheritance-modifier {property_body};  
}  
  
```  
  
### 매개 변수  
 `type`  
 속성 값의 데이터 형식 및 결과적으로 속성 자체입니다.  
  
 `property_name`  
 속성의 이름입니다.  
  
 `access-modifier`  
 액세스 한정자입니다.  유효한 한정자는 `static` 및 `virtual`입니다.  
  
 get 또는 set 접근자는 `virtual` 한정자와 일치할 필요가 지만 `static` 한정자와 일치해야 합니다.  
  
 `inheritance-modifier`  
 상속 한정자입니다.  유효한 한정자는 `abstract` 및 `sealed`입니다.  
  
 `index_list`  
 인덱스 하나 이상의 쉼표로 구분된 목록입니다.  각 인덱스는 인덱스 형식 및 속성 메서드 본문에서 사용할 수 있는 선택적 식별자로 구성됩니다.  
  
 `value`  
 set 작업에서 속성에 할당하거나 get 작업에서 검색할 값입니다.  
  
 `property_body`  
 set 또는 get 접근자의 속성 메서드 본문입니다.  `property_body`에서는 `index_list`를 기본 속성 데이터 멤버에 액세스하는 데 사용하거나 사용자 정의 처리에서 매개 변수로 사용할 수 있습니다.  
  
## [!INCLUDE[wrt](../atl/reference/includes/wrt_md.md)]  
 자세한 내용은 [속성\(C\+\+\/CX\)](http://msdn.microsoft.com/library/windows/apps/hh755807.aspx)을 참조하세요.  
  
### 요구 사항  
 컴파일러 옵션: **\/ZW**  
  
## [!INCLUDE[clr_for_headings](../dotnet/includes/clr_for_headings_md.md)]  
 **구문**  
  
```  
  
modifier property type property_name;  
  
modifier property type property_name {  
   modifier void set(type);  
   modifier type get();  
}  
modifier property type property_name[index-list, value] {  
   modifier void set(index-list, value);  
   modifier type get(index-list);  
  
modifier property type default[index];  
}  
```  
  
 **매개 변수**  
  
 *modifier*  
 속성 선언 또는 get\/set 접근자 메서드에 사용할 수 있는 한정자입니다.  가능한 값은 `static`와 `virtual`입니다.  
  
 *형식*  
 속성으로 나타내는 값의 형식입니다.  
  
 *property\_name*  
 raise 메서드에 대한 매개 변수는 대리자의 서명과 일치해야 합니다.  
  
 *index\_list*  
 대괄호\(아래 첨자 연산자, \(\[\]\)\) 안에 지정된 인덱스 하나 이상의 쉼표로 구분된 목록입니다.  각 인덱스의 경우 형식 및 선택적으로 속성 메서드 본문에서 사용할 수 있는 식별자를 지정합니다.  
  
 **설명**  
  
 첫 번째 구문 예제에서는 `set` 및 `get` 메서드를 둘 다 명시적으로 선언하는 *단순 속성*을 보여 줍니다.  컴파일러에서는 속성 값을 저장할 전용 필드를 자동으로 만듭니다.  
  
 두 번째 구문 예제에서는 `set` 및 `get` 메서드를 둘 다 명시적으로 선언하는 *속성 블록*을 보여 줍니다.  
  
 세 번째 구문 예제에서는 고객이 정의한 *인덱스 속성*을 보여 줍니다.  인덱스 속성은 설정 또는 검색할 값 이외에 매개 변수를 사용합니다.  속성 이름을 지정해야 합니다.  단순 속성과 달리 인덱스 속성의 `set` 및\/또는 `get` 메서드는 명시적으로 정의해야 하고 속성 이름을 지정해야 합니다.  
  
 네 번째 구문 예제에서는 형식 인스턴스에 대한 배열 유사 액세스를 제공하는 *기본* 속성을 보여 줍니다.  키워드 `default`는 기본 속성을 지정하는 데만 사용됩니다.  기본 속성의 이름은 속성이 정의된 형식의 이름입니다.  
  
 `property` 키워드는 클래스, 인터페이스 또는 값 형식에 표시될 수 있습니다.  속성은 get 함수\(읽기 전용\), set 함수\(쓰기 전용\) 또는 두 가지 모두\(읽기\/쓰기\)를 포함할 수 있습니다.  
  
 속성 이름은 자신이 포함된 관리되는 클래스의 이름과 일치할 수 없습니다.  getter 함수의 반환 형식은 해당 setter 함수의 마지막 매개 변수 형식과 반드시 일치해야 합니다.  
  
 클라이언트 코드에서 속성은 일반 데이터 멤버 형태로 표시되고 데이터 멤버와 같은 구문을 사용하여 쓰거나 읽을 수 있습니다.  
  
 get 및 set 메서드는 `virtual` 한정자와 일치할 필요가 없습니다.  
  
 get 및 set 메서드의 접근성은 다를 수 있습니다.  
  
 속성 메서드의 정의는 일반 메서드처럼 클래스 본문 외부에 나타날 수 있습니다.  
  
 속성에 대한 get 및 set 메서드는 **static** 한정자와 일치해야 합니다.  
  
 속성의 get 및 set 메서드가 다음 설명에 해당하면 속성은 스칼라 속성입니다.  
  
-   get 메서드에 매개 변수가 없고 반환 형식은 `T`입니다.  
  
-   set 메서드에 `T` 형식의 매개 변수가 있고 반환 형식은 **void**입니다.  
  
 같은 식별자가 포함된 한 범위에 선언된 스칼라 속성은 하나만 있어야 합니다.  스칼라 속성은 오버로드할 수 없습니다.  
  
 속성 데이터 멤버가 선언되면 컴파일러에서는 데이터 멤버\(“백업 저장소”라고도 함\)를 클래스에 주입합니다.  그러나 데이터 멤버의 이름은 포함하는 클래스의 실제 데이터 멤버였던 것처럼 소스에서 멤버를 참조할 수 없는 형태입니다.  ildasm.exe를 사용하여 형식에 대한 메타데이터를 표시하고 속성 백업 저장소의 컴파일러에서 생성된 이름을 확인합니다.  
  
 속성 블록에서 접근자 메서드에 대해 서로 다른 접근성을 사용할 수 있습니다.  즉, set 메서드는 공용일 수 있고 get 메서드는 전용일 수 있습니다.  그러나 접근자 메서드에 속성 자체의 선언에 대한 접근성보다 덜 제한적인 접근성을 포함하면 오류가 발생합니다.  
  
 `property`는 상황에 맞는 키워드입니다.  자세한 내용은 [상황에 맞는 키워드](../windows/context-sensitive-keywords-cpp-component-extensions.md)를 참조하세요.  
  
 속성에 대한 자세한 내용은 다음을 참조하세요.  
  
-   [인덱싱된 속성](../misc/how-to-use-indexed-properties.md)  
  
-   [정적 속성](../misc/how-to-declare-and-use-static-properties.md)  
  
-   [가상 속성](../misc/how-to-declare-and-use-virtual-properties.md)  
  
-   [다차원 속성](../misc/how-to-use-multidimensional-properties.md)  
  
-   [속성 접근자 메서드 오버로드](../misc/how-to-overload-property-accessor-methods.md)  
  
-   [방법: 추상 속성 및 봉인된 속성 선언](../misc/how-to-declare-abstract-and-sealed-properties.md)  
  
### 요구 사항  
 컴파일러 옵션: **\/clr**  
  
### 예  
 다음 예제에서는 속성 데이터 멤버 및 속성 블록의 선언 및 사용을 보여 줍니다.  속성 접근자를 클래스 외부에서 정의할 수 있다는 것도 보여 줍니다.  
  
```  
// mcppv2_property.cpp  
// compile with: /clr  
using namespace System;  
public ref class C {  
   int MyInt;  
public:  
  
   // property data member  
   property String ^ Simple_Property;  
  
   // property block  
   property int Property_Block {  
  
      int get();  
  
      void set(int value) {  
         MyInt = value;  
      }  
   }  
};  
  
int C::Property_Block::get() {  
   return MyInt;  
}  
  
int main() {  
   C ^ MyC = gcnew C();  
   MyC->Simple_Property = "test";  
   Console::WriteLine(MyC->Simple_Property);  
  
   MyC->Property_Block = 21;  
   Console::WriteLine(MyC->Property_Block);  
}  
```  
  
 **출력**  
  
  **테스트**  
 **21**   
## 참고 항목  
 [Component Extensions for Runtime Platforms](../windows/component-extensions-for-runtime-platforms.md)