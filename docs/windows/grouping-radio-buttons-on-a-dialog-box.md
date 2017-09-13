---
title: "Grouping Radio Buttons on a Dialog Box | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vc.editors.dialog.grouping"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "member variables, adding to radio button groups"
  - "variables, dialog box control member variables"
  - "dialog box controls, grouping radio buttons"
  - "grouping controls"
  - "radio buttons, grouping on dialog boxes"
ms.assetid: 3cc43f9e-56c8-4faa-9930-ce81733c69de
caps.latest.revision: 10
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 6
---
# Grouping Radio Buttons on a Dialog Box
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

대화 상자에 라디오 단추를 추가할 경우 그룹의 첫 번째 단추에 대한 속성 창에서 그룹 속성을 설정하여 라디오 단추를 그룹으로 처리합니다. 그러면 해당 라디오 단추의 컨트롤 ID가 [멤버 변수 추가 마법사](../ide/add-member-variable-wizard.md)에 표시됩니다. 이 마법사를 통해 라디오 단추 그룹에 대한 멤버 변수를 추가할 수 있습니다.  
  
 대화 상자에 라디오 단추 그룹이 두 개 이상 표시될 수 있으며, 각 그룹은 다음 절차에 따라 추가해야 합니다.  
  
### 대화 상자에 라디오 단추 그룹을 추가하려면  
  
1.  [도구 상자 창](../Topic/Toolbox.md)에서 라디오 단추 컨트롤을 선택하고 대화 상자에서 컨트롤을 배치하려는 위치를 클릭합니다.  
  
2.  라디오 단추를 필요한 만큼 추가하려면 1단계를 반복합니다. 그룹의 라디오 단추가 탭 순서로 연속되어 있는지 확인합니다\(자세한 내용은 [컨트롤의 탭 순서 변경](../mfc/changing-the-tab-order-of-controls.md) 참조\).  
  
3.  [속성 창](../Topic/Properties%20Window.md)에서, 탭 순서 중 *첫 번째* 라디오 단추의 **그룹** 속성을 **True**로 설정합니다.  
  
     **그룹** 속성을 **True**로 변경하면 리소스 스크립트의 대화 상자 개체에서 단추의 항목에 WS\_GROUP 스타일이 추가되며, 사용자가 단추 그룹에서 한 번에 하나의 라디오 단추만 선택할 수 있게 됩니다\(사용자가 라디오 단추를 하나 클릭하면 그룹의 다른 단추는 선택되지 않음\).  
  
    > [!NOTE]
    >  그룹의 첫 번째 라디오 단추만 **그룹** 속성이 **True**로 설정되어야 합니다. 단추 그룹에 포함되지 않은 추가 컨트롤이 있는 경우 *그룹 외부에 있는* 첫 번째 컨트롤의 **그룹** 속성을 **True**로 설정합니다. 탭 순서를 보려면 CTRL\+D를 눌러 그룹 외부의 첫 번째 컨트롤을 빠르게 확인할 수 있습니다.  
  
### 라디오 단추 그룹의 멤버 변수를 추가하려면  
  
1.  탭 순서의 첫 번째 라디오 단추 컨트롤\(기준 컨트롤이며 **그룹** 속성을 True로 설정한 컨트롤\)을 마우스 오른쪽 단추로 클릭합니다.  
  
2.  바로 가기 메뉴에서 **변수 추가**를 선택합니다.  
  
3.  [멤버 변수 추가 마법사](../ide/add-member-variable-wizard.md)에서 **제어 변수** 확인란을 선택한 후 **값** 라디오 단추를 선택합니다.  
  
4.  **변수 이름** 상자에 새 멤버 변수 이름을 입력합니다.  
  
5.  **변수 형식** 목록 상자에서 **int**를 선택하거나 **int**를 입력합니다.  
  
6.  이제 선택된 상태로 표시할 라디오 단추를 지정하도록 코드를 수정할 수 있습니다. 예를 들어 m\_radioBox1 \= 0은 그룹의 첫 번째 라디오 단추를 선택합니다.  
  
 관리되는 프로젝트에 리소스를 추가하는 방법은 *.NET Framework 개발자 가이드*에서 [응용 프로그램의 리소스](../Topic/Resources%20in%20Desktop%20Apps.md)를 참조하세요. 관리되는 프로젝트에 리소스 파일 추가, 리소스 액세스, 정적 리소스 표시, 속성에 리소스 문자열 할당 등의 작업을 수동으로 수행하는 방법에 대한 자세한 내용은 [연습: Windows Forms 지역화](http://msdn.microsoft.com/ko-kr/9a96220d-a19b-4de0-9f48-01e5d82679e5) 및 [Walkthrough: Using Resources for Localization with ASP.NET](../Topic/Walkthrough:%20Using%20Resources%20for%20Localization%20with%20ASP.NET.md)을 참조하세요.  
  
 요구 사항  
  
 Win32  
  
## 참고 항목  
 [Arrangement of Controls on Dialog Boxes](../mfc/arrangement-of-controls-on-dialog-boxes.md)   
 [Controls in Dialog Boxes](../mfc/controls-in-dialog-boxes.md)   
 [컨트롤](../mfc/controls-mfc.md)