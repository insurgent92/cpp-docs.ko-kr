---
title: "입력-출력 스트림 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- C++
helpviewer_keywords:
- I/O [C++], stream
- stream I/O
ms.assetid: 21a97566-91a7-42d6-b2f8-a4c16bc926f1
caps.latest.revision: 11
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
ms.sourcegitcommit: 3168772cbb7e8127523bc2fc2da5cc9b4f59beb8
ms.openlocfilehash: 4fdfb4ece713c071a4b740127428c16303c0ab10
ms.contentlocale: ko-kr
ms.lasthandoff: 02/24/2017

---
# <a name="inputoutput-streams"></a>입력/출력 스트림
헤더 파일 \<istream>에 정의된 `basic_iostream`은 입력 및 출력 문자 기반 I/O 스트림을 처리하는 개체에 대한 클래스 템플릿입니다.  
  
 `basic_iostream`의 문자 관련 특수화를 정의하고 코드를 더 쉽게 읽을 수 있도록 하는 형식 정의에는 두 가지가 있습니다. `iostream`(헤더 파일 \<iostream>과 혼동해서는 안 됨)은 `basic_iostream<char>`에 기반한 I/O 스트림이고, `wiostream`은 `basic_iostream<wchar_t>`에 기반한 I/O 스트림입니다.  
  
 자세한 내용은 [basic_iostream 클래스](../standard-library/basic-iostream-class.md), [iostream](../standard-library/basic-iostream-class.md) 및 [wiostream](../standard-library/basic-iostream-class.md)을 참조하세요.  
  
 `basic_iostream`에서 파생은 클래스 템플릿 `basic_fstream`이며, 파일 간에 문자 데이터를 스트림하는 데 사용됩니다.  
  
 `basic_fstream`의 문자 관련 특수화를 제공하는 형식 정의도 있습니다. 이러한 형식 정의는 `char`에 기반한 파일 I/O 스트림인 `fstream`과 `wchar_t`에 기반한 파일 I/O 스트림인 `wfstream`입니다. 자세한 내용은 [basic_fstream 클래스](../standard-library/basic-fstream-class.md), [fstream](../standard-library/basic-fstream-class.md) 및 [wfstream](../standard-library/basic-fstream-class.md)을 참조하세요. 이러한 형식 정의를 사용하려면 헤더 파일 \<fstream>을 포함해야 합니다.  
  
> [!NOTE]
>  `basic_fstream` 개체를 사용하여 파일 I/O를 수행하는 경우 기본 버퍼에 읽기 및 쓰기를 위해 별도로 지정된 위치가 포함되어 있어도 현재 입력 및 현재 출력 위치가 함께 연결되어 있으므로 일부 데이터를 읽으면 출력 위치가 이동합니다.  
  
 클래스 템플릿 `basic_stringstream` 및 해당 공용 특수화 `stringstream`은 I/O 스트림 개체를 사용하여 문자 데이터를 삽입하고 추출하는 데 자주 사용됩니다. 자세한 내용은 [basic_stringstream 클래스](../standard-library/basic-stringstream-class.md)를 참조하세요.  
  
## <a name="see-also"></a>참고 항목  
 [stringstream](../standard-library/basic-stringstream-class.md)   
 [basic_stringstream 클래스](../standard-library/basic-stringstream-class.md)   
 [\<sstream>](../standard-library/sstream.md)   
 [iostream 프로그래밍](../standard-library/iostream-programming.md)   
 [C++ 표준 라이브러리](../standard-library/cpp-standard-library-reference.md)



