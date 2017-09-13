---
title: "IOpenRowsetImpl::CreateRowset | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "IOpenRowsetImpl.CreateRowset"
  - "IOpenRowsetImpl::CreateRowset"
  - "CreateRowset"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "CreateRowset 메서드"
ms.assetid: 69041cf6-7a2f-4409-a26e-6e984c24986e
caps.latest.revision: 8
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 8
---
# IOpenRowsetImpl::CreateRowset
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

Creates a rowset object.  Not called directly by user.  See [IOpenRowset::OpenRowset](https://msdn.microsoft.com/en-us/library/ms716724.aspx) in the *OLE DB Programmer's Reference.*  
  
## 구문  
  
```  
  
      template <class   
      RowsetClass  
      >  
HRESULT CreateRowset(  
   IUnknown* pUnkOuter,  
   DBID* pTableID,  
   DBID* pIndexID,  
   REFIID riid,  
   ULONG cPropertySets,  
   DBPROPSET rgPropertySets[],  
   IUnknown** ppRowset,  
   RowsetClass*& pRowsetObj   
);  
```  
  
#### 매개 변수  
 `RowsetClass`  
 A template class member representing the user's rowset class.  Usually generated by the wizard.  
  
 `pRowsetObj`  
 \[out\] A pointer to a rowset object.  Typically this parameter is not used, but it can be used if you must perform more work on the rowset before passing it to a COM object.  The lifetime of `pRowsetObj` is bound by `ppRowset`.  
  
 For other parameters, see [IOpenRowset::OpenRowset](https://msdn.microsoft.com/en-us/library/ms716724.aspx) in the *OLE DB Programmer's Reference.*  
  
## 요구 사항  
 **Header:** atldb.h  
  
## 참고 항목  
 [IOpenRowsetImpl 클래스](../../data/oledb/iopenrowsetimpl-class.md)