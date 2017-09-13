---
title: 'How to: Configure Visual C++ Projects to Target 64-Bit, x64 Platforms | Microsoft Docs'
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- C++
helpviewer_keywords:
- platforms [C++], 64-bit
- 64-bit programming [C++], configuring projects
- project configurations [C++]
ms.assetid: 2b9ae001-df36-4750-83b2-982145d632ad
caps.latest.revision: 22
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.ht:
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- ru-ru
- zh-cn
- zh-tw
translation.priority.mt:
- cs-cz
- pl-pl
- pt-br
- tr-tr
ms.translationtype: HT
ms.sourcegitcommit: a43e0425c129cf99ed2374845a4350017bebb188
ms.openlocfilehash: 835f5f5b2fcfacb162fddaa902c7a1070e9d3773
ms.contentlocale: ko-kr
ms.lasthandoff: 08/30/2017

---
# <a name="how-to-configure-visual-c-projects-to-target-64-bit-x64-platforms"></a>How to: Configure Visual C++ Projects to Target 64-Bit, x64 Platforms

You can use the project configurations in the Visual Studio IDE to set up C++ applications to target 64-bit, x64 platforms. You can also migrate Win32 project settings into a 64-bit project configuration.  
  
### <a name="to-set-up-c-applications-to-target-64-bit-platforms"></a>To set up C++ applications to target 64-bit platforms  
  
1.  Open the C++ project that you want to configure.  
  
2.  Open the property pages for that project. For more information, see [Working with Project Properties](../ide/working-with-project-properties.md).  
  
    > [!NOTE]
    >  For .NET projects, make sure that the **Configuration Properties** node, or one of its child nodes, is selected in the **\<Projectname> Property Pages** dialog box; otherwise, the **Configuration Manager** button remains unavailable.  
  
3.  Choose the **Configuration Manager** button to open the **Configuration Manager** dialog box.  
  
4.  In the **Active Solution Platform** drop-down list, select the **\<New...>** option to open the **New Solution Platform** dialog box.  
  
5.  In the **Type or select the new platform** drop-down list, select a 64-bit target platform.  
  
    > [!NOTE]
    >  In the **New Solution Platform** dialog box, you can use the **Copy settings from** option to copy existing project settings into the new 64-bit project configuration.  
  
6.  Choose the **OK** button. The platform that you selected in the preceding step appears under **Active Solution Platform** in the **Configuration Manager** dialog box.  
  
7.  Choose the **Close** button in the **Configuration Manager** dialog box, and then choose the **OK** button in the **\<Projectname> Property Pages** dialog box.  
  
### <a name="to-copy-win32-project-settings-into-a-64-bit-project-configuration"></a>To copy Win32 project settings into a 64-bit project configuration  
  
-   When the **New Solution Platform** dialog box is open while you set up a project to target a 64-bit platform, in the **Copy settings from** drop-down list, select **Win32**. These project settings are automatically updated on the project level:  
  
    -   The [/MACHINE](../build/reference/machine-specify-target-platform.md) linker option is set to **/MACHINE:X64**.  
  
    -   **Register Output** is turned OFF. For more information, see [Linker Property Pages](../ide/linker-property-pages.md).  
  
    -   **Target Environment** is set to **/env x64**. For more information, see [MIDL Property Pages: General](../ide/midl-property-pages-general.md).  
  
    -   **Validate Parameters** is cleared and reset to the default value. For more information, see [MIDL Property Pages: Advanced](../ide/midl-property-pages-advanced.md).  
  
    -   If **Debug Information Format** was set to **/ZI** in the Win32 project configuration, then it is set to **/Zi** in the 64-bit project configuration. For more information, see [/Z7, /Zi, /ZI (Debug Information Format)](../build/reference/z7-zi-zi-debug-information-format.md).  
  
    > [!NOTE]
    >  None of these project properties are changed if they are overridden on the file level.  
  
## <a name="see-also"></a>See Also  

[.NET Framework 64-bit Applications](/dotnet/framework/64-bit-apps)   
[Configure Visual C++ for 64-bit, x64 targets](../build/configuring-programs-for-64-bit-visual-cpp.md)   
[Debug 64-Bit Applications](/visualstudio/debugger/debug-64-bit-applications)