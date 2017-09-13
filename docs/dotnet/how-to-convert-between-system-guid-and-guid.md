---
title: "방법: System::Guid 및 _GUID 사이에 변환 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "get-started-article"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "GUID, System::GUID로 변환"
  - "System::GUID"
  - "System::GUID, GUID로 변환"
ms.assetid: 022c934c-3395-4f04-b498-85ad9bf8c646
caps.latest.revision: 10
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 8
---
# 방법: System::Guid 및 _GUID 사이에 변환
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

다음 코드 예제에서는 <xref:System.Guid>와 `_GUID` 사이에서 변환하는 방법을 보여 줍니다.  
  
## 예제  
  
```  
// convert_guids.cpp  
// compile with: /clr  
#include <windows.h>  
#include <stdio.h>  
  
using namespace System;  
  
Guid FromGUID( _GUID& guid ) {  
   return Guid( guid.Data1, guid.Data2, guid.Data3,   
                guid.Data4[ 0 ], guid.Data4[ 1 ],   
                guid.Data4[ 2 ], guid.Data4[ 3 ],   
                guid.Data4[ 4 ], guid.Data4[ 5 ],   
                guid.Data4[ 6 ], guid.Data4[ 7 ] );  
}  
  
_GUID ToGUID( Guid& guid ) {  
   array<Byte>^ guidData = guid.ToByteArray();  
   pin_ptr<Byte> data = &(guidData[ 0 ]);  
  
   return *(_GUID *)data;  
}  
  
int main() {  
   _GUID ng = {0x11111111,0x2222,0x3333,0x44,0x55,0x55,0x55,0x55,0x55,0x55,0x55};  
   Guid mg;  
  
   Console::WriteLine( (mg = FromGUID( ng )).ToString() );  
   _GUID ng2 = ToGUID( mg );  
  
   printf_s(  "%x-%x-%x-", ng2.Data1, ng2.Data2, ng2.Data3 );  
   for (int i = 0 ; i < 8 ; i++) {  
      if (i == 2)  
         printf_s("-");  
      printf_s("%x", ng2.Data4[i]);  
   }  
   printf_s("\n");  
}  
```  
  
  **11111111\-2222\-3333\-4455\-555555555555**  
**11111111\-2222\-3333\-4455\-555555555555**   
## 참고 항목  
 [C\+\+ Interop 사용\(암시적 PInvoke\)](../dotnet/using-cpp-interop-implicit-pinvoke.md)