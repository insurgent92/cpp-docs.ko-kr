---
title: "상속 키워드 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "language-reference"
f1_keywords: 
  - "__multiple_inheritance"
  - "__single_inheritance_cpp"
  - "__virtual_inheritance_cpp"
  - "__virtual_inheritance"
  - "__multiple_inheritance_cpp"
  - "__single_inheritance"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "__multiple_inheritance 키워드[C++]"
  - "__single_inheritance 키워드[C++]"
  - "__virtual_inheritance 키워드[C++]"
  - "파생 클래스 선언"
  - "파생 클래스, 선언"
  - "상속, 파생 클래스 선언"
  - "상속, 키워드"
  - "키워드[C++], 상속 키워드"
ms.assetid: bb810f56-7720-4fea-b8b6-9499edd141df
caps.latest.revision: 9
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 9
---
# 상속 키워드
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

**Microsoft 전용**  
  
```  
  
class [__single_inheritance] class-name; class [__multiple_inheritance] class-name; class [__virtual_inheritance] class-name;  
```  
  
 다음은 각 문자에 대한 설명입니다.  
  
 *class\-name*  
 선언되는 클래스의 이름입니다.  
  
 C\+\+를 사용하면 클래스의 정의 이전에 클래스 멤버에 대한 포인터를 선언할 수 있습니다.  예를 들면 다음과 같습니다.  
  
```  
class S;  
int S::*p;  
```  
  
 위의 코드에서 `p`는 class S의 정수 멤버에 대한 포인터로 선언됩니다.  하지만 `class S`는 아직 이 코드에서 정의되어 있지 않으며 선언만 되어 있습니다.  컴파일러는 이러한 포인터를 발견하면 포인터의 일반화된 표현을 만들어야 합니다.  표현의 크기는 지정된 상속 모델에 따라 달라집니다.  상속 모델을 컴파일러에 지정하는 방법에는 다음 네 가지가 있습니다.  
  
-   IDE의 **멤버 포인터 표현**에서  
  
-   명령줄에서 [\/vmg](../build/reference/vmb-vmg-representation-method.md) 스위치 사용  
  
-   [pointers\_to\_members](../preprocessor/pointers-to-members.md) pragma 사용  
  
-   상속 키워드 `__single_inheritance`, `__multiple_inheritance` 및 `__virtual_inheritance` 사용.  이 방법은 클래스별로 상속 모델을 제어합니다.  
  
    > [!NOTE]
    >  항상 클래스를 정의한 후 클래스 멤버에 대한 포인터를 선언하면 이러한 옵션을 사용할 필요가 없습니다.  
  
 클래스 정의 이전에 클래스 멤버에 대한 포인터를 선언하면 결과 실행 파일의 크기와 속도가 영향을 받습니다.  클래스에서 사용하는 상속이 복잡할수록 클래스 멤버에 대한 포인터를 표현하는 데 필요한 바이트 수가 증가하고 포인터를 해석하는 데 필요한 코드가 커집니다.  단일 상속이 복잡도가 가장 낮고 가상 상속이 가장 복잡합니다.  
  
 위의 예제를 다음과 같이 변경한 경우  
  
```  
class __single_inheritance S;  
int S::*p;  
```  
  
 명령줄 옵션이나 pragma에 관계없이 `class S`의 멤버에 대한 포인터는 가장 작은 가능한 표현을 사용합니다.  
  
> [!NOTE]
>  클래스 멤버 포인터 표현의 동일한 정방향 선언이 해당 클래스의 멤버에 대한 포인터를 선언하는 각 변환 단위에서 발생해야 하며, 이 선언은 멤버에 대한 포인터가 선언되기 전에 발생해야 합니다.  
  
 **Microsoft 전용 종료**  
  
## 참고 항목  
 [C\+\+ 키워드](../cpp/keywords-cpp.md)