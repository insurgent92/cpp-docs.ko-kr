---
title: "multimap::erase(STL/CLR) | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "reference"
f1_keywords: 
  - "cliext::multimap::erase"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "erase 멤버[STL/CLR]"
ms.assetid: 94623cfc-4464-44a6-afd4-90a36828ac2b
caps.latest.revision: 16
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 14
---
# multimap::erase(STL/CLR)
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

지정된 위치에 있는 요소를 제거합니다.  
  
## 구문  
  
```  
iterator erase(iterator where);  
iterator erase(iterator first, iterator last);  
bool erase(key_type key)  
```  
  
#### 매개 변수  
 first  
 Beginning of range to erase.  
  
 key  
 Key value to erase.  
  
 last  
 End of range to erase.  
  
 where  
 Element to erase.  
  
## 설명  
 The first member function removes the element of the controlled sequence pointed to by `where`, and returns an iterator that designates the first element remaining beyond the element removed, or [multimap::end](../dotnet/multimap-end-stl-clr.md)`()` if no such element exists.  You use it to remove a single element.  
  
 The second member function removes the elements of the controlled sequence in the range `[``first``,` `last``)`, and returns an iterator that designates the first element remaining beyond any elements removed, or `end()` if no such element exists..  You use it to remove zero or more contiguous elements.  
  
 The third member function removes any element of the controlled sequence whose key has equivalent ordering to `key`, and returns a count of the number of elements removed.  You use it to remove and count all elements that match a specified key.  
  
 Each element erasure takes time proportional to the logarithm of the number of elements in the controlled sequence.  
  
## 예제  
  
```  
// cliext_multimap_erase.cpp   
// compile with: /clr   
#include <cliext/map>   
  
typedef cliext::multimap<wchar_t, int> Mymultimap;   
int main()   
    {   
    cliext::multimap<wchar_t, int> c1;   
    c1.insert(cliext::multimap<wchar_t, int>::make_value(L'a', 1));   
    c1.insert(cliext::multimap<wchar_t, int>::make_value(L'b', 2));   
    c1.insert(cliext::multimap<wchar_t, int>::make_value(L'c', 3));   
  
// display contents " [a 1] [b 2] [c 3]"   
    for each (cliext::multimap<wchar_t, int>::value_type elem in c1)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
  
// erase an element and reinspect   
    cliext::multimap<wchar_t, int>::iterator it =   
        c1.erase(c1.begin());   
    System::Console::WriteLine("erase(begin()) = [{0} {1}]",   
        it->first, it->second);   
  
// add elements and display " b c d e"   
    c1.insert(cliext::multimap<wchar_t, int>::make_value(L'd', 4));   
    c1.insert(cliext::multimap<wchar_t, int>::make_value(L'e', 5));   
    for each (cliext::multimap<wchar_t, int>::value_type elem in c1)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
  
// erase all but end   
    it = c1.end();   
    it = c1.erase(c1.begin(), --it);   
    System::Console::WriteLine("erase(begin(), end()-1) = [{0} {1}]",   
        it->first, it->second);   
    System::Console::WriteLine("size() = {0}", c1.size());   
  
// erase end   
    System::Console::WriteLine("erase(L'x') = {0}", c1.erase(L'x'));   
    System::Console::WriteLine("erase(L'e') = {0}", c1.erase(L'e'));   
    return (0);   
    }  
  
```  
  
  **\[a 1\] \[b 2\] \[c 3\]**  
**erase\(begin\(\)\) \= \[b 2\]**  
 **\[b 2\] \[c 3\] \[d 4\] \[e 5\]**  
**erase\(begin\(\), end\(\)\-1\) \= \[e 5\]**  
**size\(\) \= 1**  
**erase\(L'x'\) \= 0**  
**erase\(L'e'\) \= 1**   
## 요구 사항  
 **Header:** \<cliext\/map\>  
  
 **Namespace:** cliext  
  
## 참고 항목  
 [multimap](../dotnet/multimap-stl-clr.md)   
 [multimap::clear](../dotnet/multimap-clear-stl-clr.md)