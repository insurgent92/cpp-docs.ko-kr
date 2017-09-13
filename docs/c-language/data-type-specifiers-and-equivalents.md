---
title: "데이터 형식 지정자 및 해당 항목 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-language
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- C++
helpviewer_keywords:
- type specifiers [C++], list
- widening integers
- data types [C++], equivalents
- sign-extending integral types
- zero-extending
- identifiers, data type
- data types [C++], specifiers
- simple types, names
- type names [C++], simple
ms.assetid: 0d4b515a-4f68-4786-83cf-a5d43c7cb6f3
caps.latest.revision: 8
author: mikeblome
ms.author: mblome
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
ms.sourcegitcommit: a82768750e6a7837bb81edd8a51847f83c294c20
ms.openlocfilehash: de625abc04fcfde9d39205d024f09dc64d6c82ae
ms.contentlocale: ko-kr
ms.lasthandoff: 04/04/2017

---
# <a name="data-type-specifiers-and-equivalents"></a>데이터 형식 지정자 및 해당 항목
이 책에서는 일반적으로 긴 형태보다 다음 표에 나열되어 있는 형식 지정자의 형태를 사용하며, 기본적으로 `char` 형식이 서명되어 있다고 가정합니다. 따라서 이 책에 나온 `char`는 **signed char**와 동일합니다.  
  
### <a name="type-specifiers-and-equivalents"></a>형식 지정자 및 해당 값  
  
|형식 지정자|해당 값|  
|--------------------|---------------------|  
|**signed char**1|**char**|  
|**signed int**|**signed**, **int**|  
|**signed short int**|**short**, **signed short**|  
|**signed long int**|**long**, **signed long**|  
|**unsigned char**|—|  
|**unsigned int**|**unsigned**|  
|**unsigned short int**|**unsigned short**|  
|**unsigned long int**|**unsigned long**|  
|**float**|—|  
|**long double**2|—|  
  
 1   기본적으로 부호 없는 **char** 형식을 만들면(/J 컴파일러 옵션 지정) **signed char**를 **char**로 줄여 표현할 수 없습니다.  
  
 2   32비트 및 64비트 운영 체제에서 Microsoft C 컴파일러는 **long double**을 **double** 형식에 매핑합니다.  
  
 **Microsoft 전용**  
  
 /J 컴파일러 옵션을 지정하여 기본 **char** 형식을 signed에서 unsigned로 변경할 수 있습니다. 이 옵션이 적용되면, **char**는 **unsigned char**와 같은 의미가 되기 때문에, 부호 있는 문자 값을 선언하는 **signed** 키워드를 사용해야 합니다. **char** 값이 명시적으로 signed로 선언되면, /J 옵션은 이 값에 영향을 주지 않으며, 이 값이 **int** 형식으로 확장되는 경우에는 부호가 확장됩니다. **char** 형식은 **int** 형식으로 확장되면 제로 확장합니다.  
  
 **Microsoft 전용 종료**  
  
## <a name="see-also"></a>참고 항목  
 [C 형식 지정자](../c-language/c-type-specifiers.md)