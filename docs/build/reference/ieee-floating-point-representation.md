---
title: "IEEE 부동 소수점 표시 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "double 데이터 형식, 부동 소수점 표시"
  - "float 키워드"
  - "부동 소수점 숫자, IEEE 표현"
  - "IEEE 부동 소수점 표현"
  - "long double"
  - "real*10 값"
  - "real*4 값"
  - "real*8 값"
ms.assetid: 537833e8-fe05-49fc-8169-55fd0314b195
caps.latest.revision: 7
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 7
---
# IEEE 부동 소수점 표시
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

Microsoft Visual C\+\+는 IEEE 숫자 표준과 일치합니다.  세 종류의 실수가 있습니다.  Visual C\+\+에서는 real\*4와 real\*8이 사용됩니다.  real\*4는 **float**라는 단어를 사용하여 선언되고  real\*8은 **double**이라는 단어를 사용하여 선언됩니다.  Windows 32비트 프로그래밍에서 `long double` 데이터 형식은 **double**에 매핑됩니다.  그러나 어셈블리 언어는 real\*10 데이터 형식을 사용하는 계산을 지원합니다.  
  
 숫자 값은 다음과 같이 저장됩니다.  
  
|값|저장|  
|-------|--------|  
|real\*4|부호 비트, 8비트 지수, 23비트 가수|  
|real\*8|부호 비트, 11비트 지수, 52비트 가수|  
|real\*10|부호 비트, 15비트 지수, 64비트 가수|  
  
 real\*4 및 real\*8 형식에서는 메모리에 저장되지 않은 가수에 선행하는 1이 있는 것으로 간주하므로 가수는 23 또는 52비트만 저장되지만 실제로는 24 또는 53비트입니다.  real\*10 형식은 실제로 이 비트를 저장합니다.  
  
 지수는 가능한 값의 절반만큼 오차를 더합니다.  따라서 실제 지수를 구하려면 저장된 지수에서 이 오차를 뺍니다.  저장된 지수가 오차보다 작으면 실제는 음의 지수가 됩니다.  
  
 지수의 오차는 다음과 같습니다.  
  
|지수|오차|  
|--------|--------|  
|8비트\(real\*4\)|127|  
|11비트\(real\*8\)|1023|  
|15비트\(real\*10\)|16383|  
  
 이 지수들은 10의 제곱이 아니라 2의 제곱입니다.  즉, 8비트의 저장된 지수는 최대 127일 수 있습니다.  2\*\*127은 약 10\*\*38이며, 이 값은 real\*4의 실제 한계입니다.  
  
 가수는 1.XXX... 형태의 이진 소수로 저장됩니다. .  이 소수는 1보다 크거나 같고 2보다 작은 값입니다.  실수는 항상 정규화된 형태로 저장됩니다. 즉, 가수는 상위 차수 비트가 항상 1이 되도록 왼쪽으로 자리 옮김됩니다.  이 비트는 항상 1이기 때문에 real\*4 및 real\*8 형식으로 저장되지는 않아도 real\*4 및 real\*8 형식으로 간주됩니다.  십진수가 아닌 이진 소수점은 선행하는 1의 바로 오른쪽에 있는 것으로 간주됩니다.  
  
 여러 크기의 형식은 다음과 같습니다.  
  
|형식|BYTE 1|BYTE 2|BYTE 3|BYTE 4|...|BYTE 5|  
|--------|------------|------------|------------|------------|---------|------------|  
|real\*4|`SXXX XXXX`|`XMMM MMMM`|`MMMM MMMM`|`MMMM MMMM`|||  
|real\*8|`SXXX XXXX`|`XXXX MMMM`|`MMMM MMMM`|`MMMM MMMM`|...|`MMMM MMMM`|  
|real\*10|`SXXX XXXX`|`XXXX XXXX`|`1MMM MMMM`|`MMMM MMMM`|...|`MMMM MMMM`|  
  
 `S`는 부호 비트를 나타내며 `X`는 지수 비트, `M`은 가수 비트입니다.  가장 왼쪽에 있는 비트는 real\*4 및 real\*8 형식으로 간주되지만 real\*10 형식, BYTE 3의 "1"로 표시됩니다.  
  
 이진 소수점을 제대로 자리 옮김하려면 먼저 지수에서 오차를 뺀 다음 이진 소수점을 해당 비트 수만큼 오른쪽 또는 왼쪽으로 옮깁니다.  
  
## 예제  
 다음은 real\*4 형식의 예입니다.  
  
-   다음 예제에서 부호 비트는 0이고 저장된 지수는 128\(127\+1\) 또는 이진수 100 0000 0입니다.  저장된 가수는 \(1.\) 000 0000 ... 0000 0000이며, 선행하는 1과 이진 소수점이 있으므로 실제 가수는 1입니다.  
  
    ```  
                        SXXX XXXX XMMM MMMM ... MMMM MMMM  
    2   =  1  * 2**1  = 0100 0000 0000 0000 ... 0000 0000 = 4000 0000  
    ```  
  
-   부호 비트가 설정된 것 외에는 \+2와 같습니다.  모든 IEEE 형식의 부동 소수점 숫자에도 적용됩니다.  
  
    ```  
    -2  = -1  * 2**1  = 1100 0000 0000 0000 ... 0000 0000 = C000 0000  
    ```  
  
-   가수는 같고 지수는 1 증가한 값이며, 오차를 더한 값은 129 또는 이진수 100 0000 1입니다.  
  
    ```  
    4  =  1  * 2**2  = 0100 0000 1000 0000 ... 0000 0000 = 4080 0000  
    ```  
  
-   지수는 같고 가수는 절반만큼 더 큰 \(1.\) 100 0000 ...0000 0000입니다. 이 가수는 이진 소수이므로 1 1\/2이며, 소수 자릿수의 값은 1\/2, 1\/4, 1\/8 등입니다.  
  
    ```  
    6  = 1.5 * 2**2  = 0100 0000 1100 0000 ... 0000 0000 = 40C0 0000  
    ```  
  
-   지수는 다른 2의 제곱과 동일하며 가수는 2보다 1이 작은 127 또는 이진수 011 1111 1입니다.  
  
    ```  
    1  = 1   * 2**0  = 0011 1111 1000 0000 ... 0000 0000 = 3F80 0000  
    ```  
  
-   오차를 더한 지수는 126 또는 이진수 011 1111 0이며, 가수는 \(1.\) 100 0000 ... 0000 0000, 즉 1 1\/2입니다.  
  
    ```  
    .75 = 1.5 * 2**-1 = 0011 1111 0100 0000 ... 0000 0000 = 3F40 0000  
    ```  
  
-   가수에 1\/4을 나타내는 비트가 설정된 점을 제외하면 2와 동일합니다.  
  
    ```  
    2.5 = 1.25 * 2**1 = 0100 0000 0010 0000 ... 0000 0000 = 4020 0000  
    ```  
  
-   1\/10은 이진수로 반복되는 소수입니다.  가수는 1.6이고 오차를 더한 지수 값은 1.6이 16으로 나뉜다는 것을 나타냅니다. 이진수로는 011 1101 1이고 십진수로는 123입니다.  실제 지수는 123 – 127 \= –4로서 이는 곱할 인수가 2\*\*–4 \= 1\/16임을 의미합니다.  저장된 가수는 마지막 비트에서 반올림되어야 하는데, 표시할 수 없는 숫자를 가능한 정확하게 표시하기 위한 것입니다. 1\/10과 1\/100을 이진수로 정확히 나타낼 수 없는 이유는 1\/3을 십진수로 정확히 나타낼 수 없는 것과 같습니다.  
  
    ```  
    0.1 = 1.6 * 2**-4 = 0011 1101 1100 1100 ... 1100 1101 = 3DCC CCCD  
    ```  
  
-   `0  = 1.0 * 2**-128 = all zeros--a special case.`  
  
## 참고 항목  
 [부동 소수점 숫자의 정밀도가 떨어지는 이유](../../build/reference/why-floating-point-numbers-may-lose-precision.md)