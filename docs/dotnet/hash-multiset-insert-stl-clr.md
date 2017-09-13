---
title: "hash_multiset::insert(STL/CLR) | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "reference"
f1_keywords: 
  - "cliext::hash_multiset::insert"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "insert 멤버[STL/CLR]"
ms.assetid: e7254f30-a514-4ddc-bf53-38aafbe9e8eb
caps.latest.revision: 14
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 12
---
# hash_multiset::insert(STL/CLR)
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

Adds elements.  
  
## 구문  
  
```  
iterator insert(value_type val);  
iterator insert(iterator where, value_type val);  
template<typename InIter>  
    void insert(InIter first, InIter last);  
void insert(System::Collections::Generic::IEnumerable<value_type>^ right);  
```  
  
#### 매개 변수  
 first  
 Beginning of range to insert.  
  
 last  
 End of range to insert.  
  
 right  
 Enumeration to insert.  
  
 val  
 Key value to insert.  
  
 where  
 Where in container to insert \(hint only\).  
  
## 설명  
 Each of the member functions inserts a sequence specified by the remaining operands.  
  
 The first member function inserts an element with value `val`, and returns an iterator that designates the newly inserted element.  You use it to insert a single element.  
  
 The second member function inserts an element with value `val`, using `where` as a hint \(to improve performance\), and returns an iterator that designates the newly inserted element.  You use it to insert a single element which might be adjacent to an element you know.  
  
 The third member function inserts the sequence `[``first``,` `last``)`.  You use it to insert zero or more elements copied from another sequence.  
  
 The fourth member function inserts the sequence designated by the `right`.  You use it to insert a sequence described by an enumerator.  
  
 Each element insertion takes time proportional to the logarithm of the number of elements in the controlled sequence.  Insertion can occur in amortized constant time, however, given a hint that designates an element adjacent to the insertion point.  
  
## 예제  
  
```  
// cliext_hash_multiset_insert.cpp   
// compile with: /clr   
#include <cliext/hash_set>   
  
typedef cliext::hash_multiset<wchar_t> Myhash_multiset;   
int main()   
    {   
    Myhash_multiset c1;   
    c1.insert(L'a');   
    c1.insert(L'b');   
    c1.insert(L'c');   
  
// display initial contents " a b c"   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// insert a single value, unique and duplicate   
    System::Console::WriteLine("insert(L'x') = {0}",   
        *c1.insert(L'x'));   
  
    System::Console::WriteLine("insert(L'b') = {0}",   
        *c1.insert(L'b'));   
  
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// insert a single value with hint   
    System::Console::WriteLine("insert(begin(), L'y') = {0}",   
        *c1.insert(c1.begin(), L'y'));   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// insert an iterator range   
    Myhash_multiset c2;   
    Myhash_multiset::iterator it = c1.end();   
    c2.insert(c1.begin(), --it);   
    for each (wchar_t elem in c2)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// insert an enumeration   
    Myhash_multiset c3;   
    c3.insert(   // NOTE: cast is not needed   
        (System::Collections::Generic::IEnumerable<wchar_t>^)%c1);   
    for each (wchar_t elem in c3)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
  **a b c**  
**insert\(L'x'\) \= x**  
**insert\(L'b'\) \= b**  
 **a b b c x**  
**insert\(begin\(\), L'y'\) \= y**  
 **a b b c x y**  
 **a b b c x**  
 **a b b c x y**   
## 요구 사항  
 **Header:** \<cliext\/hash\_set\>  
  
 **Namespace:** cliext  
  
## 참고 항목  
 [hash\_multiset](../dotnet/hash-multiset-stl-clr.md)