---
title: "적용 단추 처리 | Microsoft Docs"
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
  - "속성 시트의 적용 단추"
  - "속성 시트, 적용 단추"
ms.assetid: 7e977015-59b8-406f-b545-aad0bfd8d55b
caps.latest.revision: 10
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 6
---
# 적용 단추 처리
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

Property sheets have a capability that standard dialog boxes do not: They allow the user to apply changes they have made before closing the property sheet.  This is done using the Apply button.  This article discusses methods you can use to implement this feature properly.  
  
 Modal dialog boxes usually apply the settings to an external object when the user clicks OK to close the dialog box.  The same is true for a property sheet: When the user clicks OK, the new settings in the property sheet take effect.  
  
 However, you may want to allow the user to save settings without having to close the property sheet dialog box.  This is the function of the Apply button.  The Apply button applies the current settings in all of the property pages to the external object, as opposed to applying only the current settings of the currently active page.  
  
 By default, the Apply button is always disabled.  You must write code to enable the Apply button at the appropriate times, and you must write code to implement the effect of Apply, as explained below.  
  
 If you do not wish to offer the Apply functionality to the user, it is not necessary to remove the Apply button.  You can leave it disabled, as will be common among applications that use standard property sheet support available in future versions of Windows.  
  
 To report a page as being modified and enable the Apply button, call **CPropertyPage::SetModified\( TRUE \)**.  If any of the pages report being modified, the Apply button will remain enabled, regardless of whether the currently active page has been modified.  
  
 You should call [CPropertyPage::SetModified](../Topic/CPropertyPage::SetModified.md) whenever the user changes any settings in the page.  One way to detect when a user changes a setting in the page is to implement change notification handlers for each of the controls in the property page, such as **EN\_CHANGE** or **BN\_CLICKED**.  
  
 To implement the effect of the Apply button, the property sheet must tell its owner, or some other external object in the application, to apply the current settings in the property pages.  At the same time, the property sheet should disable the Apply button by calling **CPropertyPage::SetModified\( FALSE \)** for all pages that applied their modifications to the external object.  
  
 For an example of this process, see the MFC General sample [PROPDLG](../top/visual-cpp-samples.md).  
  
## 참고 항목  
 [속성 시트](../mfc/property-sheets-mfc.md)