---
title: "식 계산 (C) | Microsoft Docs"
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
- expression evaluation
- expressions [C++], evaluating
ms.assetid: 9493f8cc-64a2-4284-9aaf-26eec11c4f40
caps.latest.revision: 6
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
ms.sourcegitcommit: d6eb43b2e77b11f4c85f6cf7e563fe743d2a7093
ms.openlocfilehash: a24e94fe4a5c89dad40b7253690475d0cc7bd0eb
ms.contentlocale: ko-kr
ms.lasthandoff: 05/18/2017

---
# <a name="expression-evaluation-c"></a>식 계산 (C)
할당, 단항 증가, 단항 감소 또는 함수 호출을 포함하는 식의 계산에 따른 결과(의도하지 않은 결과)가 생길 수 있습니다. "시퀀스 위치"에 도달하면 시퀀스 위치 뒤에 오는 모든 항목을 계산하기 전에 의도하지 않은 결과를 포함하여 시퀀스 위치 앞에 오는 모든 항목이 평가됩니다.  
  
 "의도하지 않은 결과"는 식을 계산하여 생기는 변경 내용입니다. 식을 계산하여 변수 값이 변경될 때마다 의도하지 않은 결과가 생깁니다. 모든 할당 연산에는 의도하지 않은 결과가 따릅니다. 외부에 표시되는 항목의 값을 변경할 경우 직접 할당에 의해 또는 포인터를 통한 간접 할당에 의해 함수 호출에 의도하지 않은 결과가 생길 수 있습니다.  
  
## <a name="see-also"></a>참고 항목  
 [피연산자 및 식](../c-language/operands-and-expressions.md)