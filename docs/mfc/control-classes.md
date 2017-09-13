---
title: "컨트롤 클래스 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vc.classes.control"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "단추, MFC 컨트롤 클래스"
  - "컨트롤 클래스"
  - "컨트롤 클래스, MFC"
  - "컨트롤[C++], MFC 컨트롤 클래스"
  - "컨트롤[MFC]"
  - "목록 상자, MFC 컨트롤 클래스"
  - "정적 디스플레이 컨트롤"
  - "텍스트, 입력할 컨트롤"
  - "사용자 입력, MFC 컨트롤 클래스"
ms.assetid: f9876606-9f5b-44cb-9135-213298d1df8f
caps.latest.revision: 10
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 6
---
# 컨트롤 클래스
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

Control classes encapsulate a wide variety of standard Windows controls ranging from static text controls to tree controls.  In addition, MFC provides some new controls, including buttons with bitmaps and control bars.  
  
 The controls whose class names end in "**Ctrl**" were new in Windows 95 and Windows NT version 3.51.  
  
## Static Display Controls  
 [CStatic](../mfc/reference/cstatic-class.md)  
 A static\-display window.  Static controls are used to label, box, or separate other controls in a dialog box or window.  They may also display graphical images rather than text or a box.  
  
## 텍스트 컨트롤  
 [CEdit](../mfc/reference/cedit-class.md)  
 An editable\-text control window.  Edit controls are used to accept textual input from the user.  
  
 [CIPAddressCtrl](../mfc/reference/cipaddressctrl-class.md)  
 Supports an edit box for manipulating an Internet Protocol \(IP\) address.  
  
 [CRichEditCtrl](../mfc/reference/cricheditctrl-class.md)  
 A control in which the user can enter and edit text.  Unlike the control encapsulated in `CEdit`, a rich edit control supports character and paragraph formatting and OLE objects.  
  
## Controls That Represent Numbers  
 [CSliderCtrl](../mfc/reference/csliderctrl-class.md)  
 A control containing a slider, which the user moves to select a value or set of values.  
  
 [CSpinButtonCtrl](../mfc/reference/cspinbuttonctrl-class.md)  
 A pair of arrow buttons the user can click to increment or decrement a value.  
  
 [CProgressCtrl](../mfc/reference/cprogressctrl-class.md)  
 Displays a rectangle that is gradually filled from left to right to indicate the progress of an operation.  
  
 [CScrollBar](../mfc/reference/cscrollbar-class.md)  
 A scroll\-bar control window.  The class provides the functionality of a scroll bar, for use as a control in a dialog box or window, through which the user can specify a position within a range.  
  
## 단추  
 [CButton](../mfc/reference/cbutton-class.md)  
 A button control window.  The class provides a programmatic interface for a push button, check box, or radio button in a dialog box or window.  
  
 [CBitmapButton](../mfc/reference/cbitmapbutton-class.md)  
 A button with a bitmap rather than a text caption.  
  
## 목록  
 [CListBox](../mfc/reference/clistbox-class.md)  
 A list\-box control window.  A list box displays a list of items that the user can view and select.  
  
 [CDragListBox](../mfc/reference/cdraglistbox-class.md)  
 Provides the functionality of a Windows list box; allows the user to move list box items, such as filenames and string literals, within the list box.  List boxes with this capability are useful for an item list in an order other than alphabetical, such as include pathnames or files in a project.  
  
 [CComboBox](../mfc/reference/ccombobox-class.md)  
 A combo\-box control window.  A combo box consists of an edit control plus a list box.  
  
 [CComboBoxEx](../mfc/reference/ccomboboxex-class.md)  
 이미지 목록에 대한 지원을 제공하여 콤보 상자 컨트롤을 확장합니다.  
  
 [CCheckListBox](../mfc/reference/cchecklistbox-class.md)  
 Displays a list of items with check boxes, which the user can check or clear, next to each item.  
  
 [CListCtrl](../mfc/reference/clistctrl-class.md)  
 Displays a collection of items, each consisting of an icon and a label, in a manner similar to the right pane of File Explorer.  
  
 [CTreeCtrl](../mfc/reference/ctreectrl-class.md)  
 Displays a hierarchical list of icons and labels arranged in a manner similar to the left pane of File Explorer.  
  
## Toolbars and Status Bars  
 [CToolBarCtrl](../mfc/reference/ctoolbarctrl-class.md)  
 Windows의 도구 모음 공용 컨트롤의 기능을 제공합니다.  Most MFC programs use [CToolBar](../mfc/reference/ctoolbar-class.md) instead of this class.  
  
 [CStatusBarCtrl](../mfc/reference/cstatusbarctrl-class.md)  
 A horizontal window, usually divided into panes, in which an application can display status information.  Most MFC programs use [CStatusBar](../mfc/reference/cstatusbar-class.md) instead of this class.  
  
## Miscellaneous Controls  
 [CAnimateCtrl](../mfc/reference/canimatectrl-class.md)  
 Displays a simple video clip.  
  
 [CToolTipCtrl](../mfc/reference/ctooltipctrl-class.md)  
 A small pop\-up window that displays a single line of text describing the purpose of a tool in an application.  
  
 [CDateTimeCtrl](../mfc/reference/cdatetimectrl-class.md)  
 Supports either an extended edit control, or a simple calendar interface control, that allows a user to choose a specific date or time value.  
  
 [CHeaderCtrl](../mfc/reference/cheaderctrl-class.md)  
 Displays titles or labels for columns.  
  
 [CMonthCalCtrl](../mfc/reference/cmonthcalctrl-class.md)  
 Supports a simple calendar interface control that allows a user to select a date.  
  
 [CTabCtrl](../mfc/reference/ctabctrl-class.md)  
 A control with tabs on which the user can click, analogous to the dividers in a notebook.  
  
 [CHotKeyCtrl](../mfc/reference/chotkeyctrl-class.md)  
 Enables the user to create a hot key combination, which the user can press to perform an action quickly.  
  
 [CLinkCtrl](../mfc/reference/clinkctrl-class.md)  
 Renders marked\-up text and launches appropriate applications when the user clicks the embedded link.  
  
 [CHtmlEditCtrl](../mfc/reference/chtmleditctrl-class.md)  
 MFC 창에서 WebBrowser ActiveX 컨트롤의 기능을 제공합니다.  
  
## Related Classes  
 [CImageList](../mfc/reference/cimagelist-class.md)  
 Provides the functionality of the Windows image list.  Image lists are used with list controls and tree controls.  They can also be used to store and archive a set of same\-sized bitmaps.  
  
 [CCtrlView](../mfc/reference/cctrlview-class.md)  
 The base class for all views associated with Windows controls.  The views based on controls are described below.  
  
 [CEditView](../mfc/reference/ceditview-class.md)  
 A view that contains a Windows standard edit control.  
  
 [CRichEditView](../mfc/reference/cricheditview-class.md)  
 A view that contains a Windows rich edit control.  
  
 [CListView](../mfc/reference/clistview-class.md)  
 A view that contains a Windows list control.  
  
 [CTreeView](../mfc/reference/ctreeview-class.md)  
 A view that contains a Windows tree control.  
  
## 참고 항목  
 [클래스 개요](../mfc/class-library-overview.md)