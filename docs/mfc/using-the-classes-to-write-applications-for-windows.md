---
title: "클래스를 사용하여 Windows 응용 프로그램 작성 | Microsoft Docs"
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
  - "응용 프로그램[OLE], MFC 응용 프로그램 프레임워크"
  - "데이터베이스 응용 프로그램[C++], 만들기"
  - "MFC[C++], 응용 프로그램 개발"
  - "MFC ActiveX 컨트롤, 만들기"
  - "OLE 응용 프로그램[C++], MFC 응용 프로그램 프레임워크"
  - "Windows 응용 프로그램[C++], MFC 응용 프로그램 프레임워크"
ms.assetid: 73f63470-857d-43dd-9a54-b38b7be0f1b7
caps.latest.revision: 10
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 6
---
# 클래스를 사용하여 Windows 응용 프로그램 작성
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

Taken together, the classes in the Microsoft Foundation Class \(MFC\) Library make up an "application framework," on which you build an application for the Windows operating system.  At a very general level, the framework defines the skeleton of an application and supplies standard user\-interface implementations that can be placed onto the skeleton.  Your job as programmer is to fill in the rest of the skeleton, which are those things that are specific to your application.  You can get a head start by using the MFC Application Wizard to create the files for a very thorough starter application.  You use the Microsoft Visual C\+\+ resource editors to design your user\-interface elements visually, Class View commands to connect those elements to code, and the class library to implement your application\-specific logic.  
  
 Version 3.0 and later of the MFC framework supports programming for Win32 platforms, including Microsoft Windows 95 and later, and Windows NT versions 3.51 and later.  MFC Win32 support includes multithreading.  Use version 1.5*x* if you need to do 16\-bit programming.  
  
 This family of articles presents a broad overview of the application framework.  It also explores the major objects that make up your application and how they are created.  Among the topics covered in these articles are the following:  
  
-   [The framework](../mfc/framework-mfc.md).  
  
-   Division of labor between the framework and your code, as described in [Building on the Framework](../mfc/building-on-the-framework.md).  
  
-   [The application class](../mfc/cwinapp-the-application-class.md), which encapsulates application\-level functionality.  
  
-   How [document templates](../mfc/document-templates-and-the-document-view-creation-process.md) create and manage documents and their associated views and frame windows.  
  
-   Class [CWnd](../mfc/window-objects.md), the root base class of all windows.  
  
-   [Graphic objects](../mfc/graphic-objects.md), such as pens and brushes.  
  
 Other parts of the framework include:  
  
-   [Window Objects: Overview](../mfc/window-objects.md)  
  
-   [Message handling and mapping](../mfc/message-handling-and-mapping.md)  
  
-   [CObject, The Root Base Class in MFC](../mfc/using-cobject.md)  
  
-   [Document\/View Architecture](../mfc/document-view-architecture.md)  
  
-   [대화 상자](../mfc/dialog-boxes.md)  
  
-   [컨트롤](../mfc/controls-mfc.md)  
  
-   [컨트롤 막대](../mfc/control-bars.md)  
  
-   [OLE](../mfc/ole-in-mfc.md)  
  
-   [메모리 관리](../mfc/memory-management.md)  
  
     Besides giving you an advantage in writing applications for the Windows operating system, MFC also makes it much easier to write applications that specifically use OLE linking and embedding technology.  You can make your application an OLE visual editing container, an OLE visual editing server, or both, and you can add Automation so that other applications can use objects from your application or even drive it remotely.  
  
-   [MFC ActiveX Controls](../mfc/mfc-activex-controls.md)  
  
     The OLE control development kit \(CDK\) is now fully integrated with the framework.  This article family supplies an overview of ActiveX control development with MFC. \(ActiveX controls were formerly known as OLE controls.\)  
  
-   [Database Programming](../data/data-access-programming-mfc-atl.md)  
  
     MFC also supplies two sets of database classes that simplify writing data\-access applications.  Using the ODBC database classes, you can connect to databases through an Open Database Connectivity \(ODBC\) driver, select records from tables, and display record information in an on\-screen form.  Using the Data Access Object \(DAO\) classes, you can work with databases through the Microsoft Jet database engine or external \(non\-Jet\) data sources, including ODBC data sources.  
  
     In addition, MFC is fully enabled for writing applications that use Unicode and multibyte character sets \(MBCS\), specifically double\-byte character sets \(DBCS\).  
  
 For a general guide to MFC documentation, see [General MFC Topics](../mfc/general-mfc-topics.md).  
  
## 참고 항목  
 [일반 MFC 항목](../mfc/general-mfc-topics.md)