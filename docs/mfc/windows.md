---
title: "Windows | Microsoft Docs"
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
  - "MFC[C++], windows"
  - "개체[C++], window"
  - "창 개체[C++], MFC 프레임워크"
  - "창[C++]"
ms.assetid: dd92bf34-842e-40fe-8aea-3028b55314d5
caps.latest.revision: 11
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 7
---
# Windows
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

This family of articles covers window objects in the MFC framework.  All MFC windows derive from class [CWnd](../mfc/reference/cwnd-class.md), including frame windows, views, dialog boxes, and controls.  
  
 The first group of articles describes [window objects](../mfc/window-objects.md) in general.  Refer to this group for general information about C\+\+ window objects, how they encapsulate an HWND, and how you use them when creating your own windows, such as child windows.  
  
 The second group of articles describes [frame windows](../mfc/frame-windows.md)—windows that put a frame around content — in particular.  Refer to this group for information about how the MFC framework manages frame windows and the contents that they frame, including control bars and views.  
  
## 추가 정보  
 *Topics on Window Objects in General*  
  
-   [Window objects](../mfc/window-objects.md)  
  
-   [Relationship between a C\+\+ window objects and HWND handles](../mfc/relationship-between-a-cpp-window-object-and-an-hwnd.md)  
  
-   [Derived Window classes](../mfc/derived-window-classes.md)  
  
-   [Creating window objects](../mfc/creating-windows.md)  
  
-   [Destroying Window Objects](../mfc/destroying-window-objects.md)  
  
-   [Registering window "classes"](../mfc/registering-window-classes.md)  
  
-   [Working with window objects](../mfc/working-with-window-objects.md)  
  
-   [Device contexts](../mfc/device-contexts.md): objects that make Windows drawing device\-independent  
  
-   [Graphic objects](../mfc/graphic-objects.md): pens, brushes, fonts, bitmaps, palettes, regions  
  
 *Frame Window Topics*  
  
-   [Frame windows](../mfc/frame-windows.md): window objects that provide frames  
  
-   [Frame windows and views](../mfc/frame-windows.md)  
  
-   [Frame\-window classes](../mfc/frame-window-classes.md)  
  
-   [Frame\-window styles](../mfc/frame-window-styles-cpp.md)  
  
-   [Changing the styles of a window created by MFC](../mfc/changing-the-styles-of-a-window-created-by-mfc.md)  
  
-   [What frame windows do](../mfc/what-frame-windows-do.md)  
  
-   [Using frame windows](../mfc/using-frame-windows.md)  
  
-   [Managing MD\/Child windows \(the MDICLIENT window\)](../mfc/managing-mdi-child-windows.md)  
  
-   [Managing menus, control bars, and accelerators](../mfc/managing-menus-control-bars-and-accelerators.md)  
  
-   [CFrameWnd](../mfc/reference/cframewnd-class.md)  
  
-   [CMDIFrameWnd](../mfc/reference/cmdiframewnd-class.md)  
  
-   [CMDIChildWnd](../mfc/reference/cmdichildwnd-class.md)  
  
-   [Using Views](../mfc/using-views.md)  
  
-   [Multiple Document Types, Views, and Frame Windows \(Splitter windows\)](../mfc/multiple-document-types-views-and-frame-windows.md)  
  
-   [Messages \(maps and handler functions\)](../mfc/messages.md)  
  
 *Create and Destroy Windows*  
  
-   [General Window Creation Sequence](../mfc/general-window-creation-sequence.md)  
  
-   [Destroy window objects](../mfc/destroying-window-objects.md)  
  
-   [Create document frame windows](../mfc/creating-document-frame-windows.md)  
  
-   [Destroy frame windows](../mfc/destroying-frame-windows.md)  
  
 *Create Splitter Windows*  
  
-   [Create splitter windows](../mfc/multiple-document-types-views-and-frame-windows.md)  
  
 *Manage Child Windows and the Current View*  
  
-   [Manage MDI child windows](../mfc/managing-mdi-child-windows.md)  
  
-   [Manage the current view](../mfc/managing-the-current-view.md)  
  
-   [Manage menus, control bars, and accelerators](../mfc/managing-menus-control-bars-and-accelerators.md)  
  
 *Work with Device Contexts and Window Styles*  
  
-   [Use pens and other graphic objects in a device context](../mfc/graphic-objects.md)  
  
-   [Change the styles of a window created by MFC](../mfc/changing-the-styles-of-a-window-created-by-mfc.md)  
  
## 참고 항목  
 [사용자 인터페이스 요소](../mfc/user-interface-elements-mfc.md)   
 [대화 상자](../mfc/dialog-boxes.md)   
 [도구 모음](../mfc/toolbars.md)   
 [상태 표시줄](../mfc/status-bars.md)   
 [대화 상자 모음](../mfc/dialog-bars.md)