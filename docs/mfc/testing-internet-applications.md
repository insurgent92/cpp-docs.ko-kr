---
title: "인터넷 응용 프로그램 테스트 | Microsoft Docs"
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
  - "디버깅[MFC], 웹 응용 프로그램"
  - "웹 응용 프로그램 디버깅, 응용 프로그램 테스트"
  - "인터넷 디버깅 및 테스트"
  - "테스트, 인터넷 응용 프로그램"
  - "웹 응용 프로그램, 테스트"
ms.assetid: ac4c74e3-d4ad-4e19-8f6c-e270de067f01
caps.latest.revision: 10
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 6
---
# 인터넷 응용 프로그램 테스트
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

There are some unique testing challenges on the Internet, especially for applications running on a Web server.  Your initial testing will probably be done using a single\-user client connecting to a test server.  This will be useful for debugging your code.  
  
 You will also want to test under real conditions: with multiple clients connected over high\-speed connections as well as low\-speed serial lines, including modem connections.  It can be difficult to simulate real conditions, but it is certainly worth spending time designing possible scenarios and executing them.  If possible, you will also want to use tools to do capacity and stress testing.  Certain classes of bugs, such as timing bugs, are difficult to find and to reproduce.  
  
 One of the challenges of Internet programming is its visibility.  Many accesses to your site may slow down your server.  You want your server to degrade gracefully.  You want to prevent anything that could be destructive to a user's computer if your application fails \(for example, corruption of data while writing to the registry or while writing cookies on the client\).  
  
## 참고 항목  
 [MFC 인터넷 프로그래밍 작업](../mfc/mfc-internet-programming-tasks.md)   
 [MFC 인터넷 프로그래밍 기본 사항](../mfc/mfc-internet-programming-basics.md)