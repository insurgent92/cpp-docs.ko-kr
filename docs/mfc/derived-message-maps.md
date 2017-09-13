---
title: "파생된 메시지 맵 | Microsoft Docs"
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
  - "파생된 메시지 맵"
  - "메시지 처리, 파생된 메시지 처리기"
  - "메시지 맵, 파생"
  - "메시지, 라우팅"
ms.assetid: 21829556-6e64-40c3-8279-fed85d99de77
caps.latest.revision: 11
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 7
---
# 파생된 메시지 맵
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

During message handling, checking a class's own message map is not the end of the message\-map story.  What happens if class `CMyView` \(derived from `CView`\) has no matching entry for a message?  
  
 Keep in mind that `CView`, the base class of `CMyView`, is derived in turn from `CWnd`.  Thus `CMyView` *is* a `CView` and *is* a `CWnd`.  Each of those classes has its own message map.  The figure "A View Hierarchy" below shows the hierarchical relationship of the classes, but keep in mind that a `CMyView` object is a single object that has the characteristics of all three classes.  
  
 ![뷰 계층 구조](../mfc/media/vc38621.png "vc38621")  
A View Hierarchy  
  
 So if a message can't be matched in class `CMyView`'s message map, the framework also searches the message map of its immediate base class.  The `BEGIN_MESSAGE_MAP` macro at the start of the message map specifies two class names as its arguments:  
  
 [!code-cpp[NVC_MFCMessageHandling#2](../mfc/codesnippet/CPP/derived-message-maps_1.cpp)]  
  
 The first argument names the class to which the message map belongs.  The second argument provides a connection with the immediate base class — `CView` here — so the framework can search its message map, too.  
  
 The message handlers provided in a base class are thus inherited by the derived class.  This is very similar to normal virtual member functions without needing to make all handler member functions virtual.  
  
 If no handler is found in any of the base\-class message maps, default processing of the message is performed.  If the message is a command, the framework routes it to the next command target.  If it is a standard Windows message, the message is passed to the appropriate default window procedure.  
  
 To speed message\-map matching, the framework caches recent matches on the likelihood that it will receive the same message again.  One consequence of this is that the framework processes unhandled messages quite efficiently.  Message maps are also more space\-efficient than implementations that use virtual functions.  
  
## 참고 항목  
 [프레임워크가 메시지 맵을 검색하는 방법](../mfc/how-the-framework-searches-message-maps.md)