---
title: "Rich Edit 컨트롤의 개요 | Microsoft Docs"
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
  - "rich edit 컨트롤"
ms.assetid: ad589b9f-a3fd-4820-bf1f-6b1965997e68
caps.latest.revision: 10
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 6
---
# Rich Edit 컨트롤의 개요
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

> [!IMPORTANT]
>  If you are using a rich edit control in a dialog box \(regardless of whether your application is SDI, MDI, or dialog\-based\), you must call [AfxInitRichEdit](../Topic/AfxInitRichEdit.md) once before the dialog box is displayed.  A typical place to call this function is in your program's `InitInstance` member function.  You do not need to call it for each time you display the dialog box, only the first time.  You do not have to call `AfxInitRichEdit` if you are working with `CRichEditView`.  
  
 Rich edit controls \([CRichEditCtrl](../mfc/reference/cricheditctrl-class.md)\) provide a programming interface for formatting text.  However, an application must implement any user interface components necessary to make formatting operations available to the user.  That is, the rich edit control supports changing the character or paragraph attributes of the selected text.  Some examples of character attributes are bold, italics, font family, and point size.  Examples of paragraph attributes include alignment, margins, and tab stops.  However, it is up to you to provide the user interface, whether that is toolbar buttons, menu items, or a format character dialog box.  There are also functions to query the rich edit control for the attributes of the current selection.  Use these functions to display the current settings for the attributes, for example, setting a check mark on the command UI if the selection has the bold character formatting attribute.  
  
 For more information on character and paragraph formatting, see [Character Formatting](../mfc/character-formatting-in-rich-edit-controls.md) and [Paragraph Formatting](../mfc/paragraph-formatting-in-rich-edit-controls.md) later in this topic.  
  
 Rich edit controls support almost all of the operations and notification messages used with multiline edit controls.  Thus, applications that already use edit controls can be easily changed to use rich edit controls.  Additional messages and notifications enable applications to access the functionality unique to rich edit controls.  For information about edit controls, see [CEdit](../mfc/reference/cedit-class.md).  
  
 For more information on notifications, see [Notifications from a Rich Edit Control](../mfc/notifications-from-a-rich-edit-control.md) later in this topic.  
  
## 참고 항목  
 [CRichEditCtrl 사용](../mfc/using-cricheditctrl.md)   
 [컨트롤](../mfc/controls-mfc.md)