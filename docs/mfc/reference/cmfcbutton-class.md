---
title: "CMFCButton 클래스 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- CMFCButton
- AFXBUTTON/CMFCButton
- AFXBUTTON/CMFCButton::CleanUp
- AFXBUTTON/CMFCButton::EnableFullTextTooltip
- AFXBUTTON/CMFCButton::EnableMenuFont
- AFXBUTTON/CMFCButton::EnableWindowsTheming
- AFXBUTTON/CMFCButton::GetToolTipCtrl
- AFXBUTTON/CMFCButton::IsAutoCheck
- AFXBUTTON/CMFCButton::IsAutorepeatCommandMode
- AFXBUTTON/CMFCButton::IsCheckBox
- AFXBUTTON/CMFCButton::IsChecked
- AFXBUTTON/CMFCButton::IsHighlighted
- AFXBUTTON/CMFCButton::IsPressed
- AFXBUTTON/CMFCButton::IsPushed
- AFXBUTTON/CMFCButton::IsRadioButton
- AFXBUTTON/CMFCButton::IsWindowsThemingEnabled
- AFXBUTTON/CMFCButton::SetAutorepeatMode
- AFXBUTTON/CMFCButton::SetCheckedImage
- AFXBUTTON/CMFCButton::SetFaceColor
- AFXBUTTON/CMFCButton::SetImage
- AFXBUTTON/CMFCButton::SetMouseCursor
- AFXBUTTON/CMFCButton::SetMouseCursorHand
- AFXBUTTON/CMFCButton::SetStdImage
- AFXBUTTON/CMFCButton::SetTextColor
- AFXBUTTON/CMFCButton::SetTextHotColor
- AFXBUTTON/CMFCButton::SetTooltip
- AFXBUTTON/CMFCButton::SizeToContent
- AFXBUTTON/CMFCButton::OnDraw
- AFXBUTTON/CMFCButton::OnDrawBorder
- AFXBUTTON/CMFCButton::OnDrawFocusRect
- AFXBUTTON/CMFCButton::OnDrawText
- AFXBUTTON/CMFCButton::OnFillBackground
- AFXBUTTON/CMFCButton::SelectFont
- AFXBUTTON/CMFCButton::m_bDrawFocus
- AFXBUTTON/CMFCButton::m_bHighlightChecked
- AFXBUTTON/CMFCButton::m_bRightImage
- AFXBUTTON/CMFCButton::m_bTransparent
- AFXBUTTON/CMFCButton::m_nAlignStyle
- AFXBUTTON/CMFCButton::m_nFlatStyle
dev_langs:
- C++
helpviewer_keywords:
- CMFCButton::CreateObject method
- CMFCButton::DrawItem method
- CMFCButton::PreTranslateMessage method
- CMFCButton constructor
- CMFCButton::OnDrawParentBackground method
- CMFCButton class
ms.assetid: 4b32f57c-7a53-4734-afb9-d47e3359f62e
caps.latest.revision: 35
author: mikeblome
ms.author: mblome
manager: ghogen
translation.priority.ht:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
ms.translationtype: Machine Translation
ms.sourcegitcommit: 0e0c08ddc57d437c51872b5186ae3fc983bb0199
ms.openlocfilehash: 89cd722ac15a1d9ac6b6c815c837559e302f0e68
ms.contentlocale: ko-kr
ms.lasthandoff: 02/24/2017

---
# <a name="cmfcbutton-class"></a>CMFCButton 클래스
`CMFCButton` 기능을 추가 하는 클래스는 [CButton](../../mfc/reference/cbutton-class.md) 단추 텍스트 정렬, 단추 텍스트 및 이미지 결합, 커서 선택, 도구 설명 지정 등 클래스입니다.  
  
## <a name="syntax"></a>구문  
  
```  
class CMFCButton : public CButton  
```  
  
## <a name="members"></a>멤버  
  
### <a name="public-constructors"></a>Public 생성자  
  
|이름|설명|  
|----------|-----------------|  
|`CMFCButton::CMFCButton`|기본 생성자입니다.|  
|`CMFCButton::~CMFCButton`|소멸자|  
  
### <a name="public-methods"></a>Public 메서드  
  
|이름|설명|  
|----------|-----------------|  
|[CMFCButton::CleanUp](#cleanup)|내부 변수를 다시 설정 하 고 이미지, 비트맵 및 아이콘 등의 할당 된 리소스를 해제 합니다.|  
|`CMFCButton::CreateObject`|프레임워크에서 이 클래스 형식의 동적 인스턴스를 만드는 데 사용합니다.|  
|`CMFCButton::DrawItem`|프레임 워크는 소유자가 그린 단추의 시각적 측면이 변경 될 때 호출 됩니다. (재정의 [CButton::DrawItem](../../mfc/reference/cbutton-class.md#drawitem).)|  
|[CMFCButton::EnableFullTextTooltip](#enablefulltexttooltip)|큰 도구 설명 창이 나 작은 도구 설명 창의 텍스트의 요약된 버전에 도구 설명의 전체 텍스트를 표시할지 여부를 지정 합니다.|  
|[CMFCButton::EnableMenuFont](#enablemenufont)|단추 텍스트 글꼴을 응용 프로그램 메뉴 글꼴로 같은지 여부를 지정 합니다.|  
|[CMFCButton::EnableWindowsTheming](#enablewindowstheming)|단추 테두리의 스타일은 현재 Windows 테마에 해당 하는지 여부를 지정 합니다.|  
|`CMFCButton::GetThisClass`|에 대 한 포인터를 가져오는 데 프레임 워크에 의해는 [CRuntimeClass](../../mfc/reference/cruntimeclass-structure.md) 이 클래스 형식으로 연결 된 개체입니다.|  
|[CMFCButton::GetToolTipCtrl](#gettooltipctrl)|기본 도구 설명 컨트롤에 대 한 참조를 반환합니다.|  
|[CMFCButton::IsAutoCheck](#isautocheck)|확인란 또는 라디오 단추는 자동 단추 인지를 나타냅니다.|  
|[CMFCButton::IsAutorepeatCommandMode](#isautorepeatcommandmode)|단추 자동 반복 모드로 설정 되어 있는지 여부를 나타냅니다.|  
|[CMFCButton::IsCheckBox](#ischeckbox)|단추 확인란 단추 인지를 나타냅니다.|  
|[CMFCButton::IsChecked](#ischecked)|현재 단추가 선택 되어 있는지를 나타냅니다.|  
|[CMFCButton::IsHighlighted](#ishighlighted)|단추가 강조 표시 하는지 여부를 나타냅니다.|  
|[CMFCButton::IsPressed](#ispressed)|단추 푸시되는 강조 표시 된 지를 나타냅니다.|  
|[CMFCButton::IsPushed](#ispushed)|단추를 누를 있는지 여부를 나타냅니다.|  
|[CMFCButton::IsRadioButton](#isradiobutton)|단추는 라디오 단추 인지를 나타냅니다.|  
|[CMFCButton::IsWindowsThemingEnabled](#iswindowsthemingenabled)|단추 테두리의 스타일은 현재 Windows 테마에 해당 하는지 여부를 나타냅니다.|  
|`CMFCButton::OnDrawParentBackground`|지정된 된 영역에는 단추의 부모의 배경을 그립니다. (재정의 [afx_global_data:: drawparentbackground](../../mfc/reference/afx-global-data-structure.md)|  
|`CMFCButton::PreTranslateMessage`|창 메시지를 변환 하 여으로 디스패치 되기 전에 [TranslateMessage](http://msdn.microsoft.com/library/windows/desktop/ms644955) 및 [DispatchMessage](http://msdn.microsoft.com/library/windows/desktop/ms644934) Windows 함수입니다. (재정의 [CWnd::PreTranslateMessage](../../mfc/reference/cwnd-class.md#pretranslatemessage).)|  
|[CMFCButton::SetAutorepeatMode](#setautorepeatmode)|단추 자동 반복 모드를 설정합니다.|  
|[CMFCButton::SetCheckedImage](#setcheckedimage)|이미지 선택된 단추를 설정합니다.|  
|[CMFCButton::SetFaceColor](#setfacecolor)|단추 텍스트의 배경색을 설정합니다.|  
|[CMFCButton::SetImage](#setimage)|단추에 대 한 이미지를 설정합니다.|  
|[CMFCButton::SetMouseCursor](#setmousecursor)|커서 이미지를 설정합니다.|  
|[CMFCButton::SetMouseCursorHand](#setmousecursorhand)|손 모양 이미지에 커서를 설정합니다.|  
|[CMFCButton::SetStdImage](#setstdimage)|사용 하 여 한 `CMenuImages` 단추 이미지를 설정 하는 개체입니다.|  
|[CMFCButton::SetTextColor](#settextcolor)|선택 되지 않은 단추에 대 한 단추 텍스트의 색을 설정 합니다.|  
|[CMFCButton::SetTextHotColor](#settexthotcolor)|선택 된 단추에 대 한 단추 텍스트의 색을 설정 합니다.|  
|[CMFCButton::SetTooltip](#settooltip)|단추를 도구 설명에 연결합니다.|  
|[CMFCButton::SizeToContent](#sizetocontent)|단추 텍스트와 이미지를 포함 하는 단추 크기가 조정 됩니다.|  
  
### <a name="protected-methods"></a>Protected 메서드  
  
|이름|설명|  
|----------|-----------------|  
|[CMFCButton::OnDraw](#ondraw)|단추를 그리는 프레임 워크에 의해 호출 됩니다.|  
|[CMFCButton::OnDrawBorder](#ondrawborder)|단추의 테두리를 그리는 프레임 워크에 의해 호출 됩니다.|  
|[CMFCButton::OnDrawFocusRect](#ondrawfocusrect)|단추에 대 한 포커스 사각형을 그리는 프레임 워크에 의해 호출 됩니다.|  
|[CMFCButton::OnDrawText](#ondrawtext)|단추 텍스트를 그릴 프레임 워크에 의해 호출 됩니다.|  
|[CMFCButton::OnFillBackground](#onfillbackground)|단추 텍스트의 배경을 그리기 위한 프레임 워크에 의해 호출 됩니다.|  
|[CMFCButton::SelectFont](#selectfont)|지정된 된 장치 컨텍스트에 연결 되는 글꼴을 가져옵니다.|  
  
### <a name="data-members"></a>데이터 멤버  
  
|이름|설명|  
|----------|-----------------|  
|[CMFCButton::m_bDrawFocus](#m_bdrawfocus)|단추 주위에 포커스 영역을 그릴 것인지를 나타냅니다.|  
|[CMFCButton::m_bHighlightChecked](#m_bhighlightchecked)|커서를 위로 이동할 때 BS_CHECKBOX 스타일 단추를 강조 표시 여부를 나타냅니다.|  
|[CMFCButton::m_bRightImage](#m_brightimage)|단추 오른쪽에 이미지를 표시할지 여부를 나타냅니다.|  
|[CMFCButton::m_bTransparent](#m_btransparent)|단추 투명 한지 여부를 나타냅니다.|  
|[CMFCButton::m_nAlignStyle](#m_nalignstyle)|단추 텍스트의 맞춤을 지정 합니다.|  
|[CMFCButton::m_nFlatStyle](#m_nflatstyle)|예: 여백, 플랫 형식의 세미콜론 평면 또는 3D 단추 스타일을 지정합니다.|  
  
## <a name="remarks"></a>주의  
 다른 종류의 단추에서 파생 되는 `CMFCButton` 클래스 같은 [CMFCURLLinkButton](../../mfc/reference/cmfclinkctrl-class.md) 하이퍼링크를 지원 하며 클래스 및 `CMFCColorButton` 색 선택 대화 상자를 지 원하는 클래스.  
  
 스타일을 `CMFCButton` 개체 일 수 *3D*, *플랫*, *세미콜론 플랫* 또는 *테두리 없음*. 단추 텍스트의 왼쪽, 위쪽, 또는 단추의 가운데에 정렬할 수 있습니다. 런타임 시 텍스트, 이미지 또는 텍스트와 이미지 단추는 표시 여부를 제어할 수 있습니다. 커서를 단추 위로 이동할 때 특정 커서 이미지를 표시 하도록 지정할 수 있습니다.  
  
 사용자 코드에서 직접 또는 사용 하 여 단추 컨트롤을 만들기는 **MFC 클래스 마법사** 도구 및 대화 상자 템플릿에 합니다. 단추 컨트롤을 직접 만드는 경우 추가 `CMFCButton` 하 고 응용 프로그램에 생성자를 호출한 다음 변수 및 `Create` 의 메서드는 `CMFCButton` 개체입니다. 사용 하는 경우는 **MFC 클래스 마법사**, 추가 `CButton` 응용 프로그램 변수에서 변수의 형식을 변경 합니다 `CButton` 를 `CMFCButton`합니다.  
  
 대화 상자 응용 프로그램에서 알림 메시지를 처리 하려면 메시지 맵 항목 및 각 알림에 대 한 이벤트 처리기를 추가 합니다. 보낸 알림의 `CMFCButton` 개체에서 보낸 것과 동일는 `CButton` 개체입니다.  
  
## <a name="example"></a>예제  
 다음 예제에서는 다양 한 메서드를 사용 하 여 단추의 속성을 구성 하는 방법의 `CMFCButton` 클래스입니다. 일부인이 예제는 [새 컨트롤 샘플](../../visual-cpp-samples.md)합니다.  
  
 [!code-cpp[NVC_MFC_NewControls #&28;](../../mfc/reference/codesnippet/cpp/cmfcbutton-class_1.h)]  
[!code-cpp[NVC_MFC_NewControls #&31;](../../mfc/reference/codesnippet/cpp/cmfcbutton-class_2.cpp)]  
[!code-cpp[NVC_MFC_NewControls #&32;](../../mfc/reference/codesnippet/cpp/cmfcbutton-class_3.cpp)]  
[!code-cpp[NVC_MFC_NewControls #&33;](../../mfc/reference/codesnippet/cpp/cmfcbutton-class_4.cpp)]  
  
## <a name="inheritance-hierarchy"></a>상속 계층  
 [CObject](../../mfc/reference/cobject-class.md)  
  
 [CCmdTarget](../../mfc/reference/ccmdtarget-class.md)  
  
 [CWnd](../../mfc/reference/cwnd-class.md)  
  
 [CButton](../../mfc/reference/cbutton-class.md)  
  
 [CMFCButton](../../mfc/reference/cmfcbutton-class.md)  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** afxbutton.h  
  
##  <a name="cleanup"></a>CMFCButton::CleanUp  
 내부 변수를 다시 설정 하 고 이미지, 비트맵 및 아이콘 등의 할당 된 리소스를 해제 합니다.  
  
```  
virtual void CleanUp();
```  
  
##  <a name="enablefulltexttooltip"></a>CMFCButton::EnableFullTextTooltip  
 큰 도구 설명 창이 나 작은 도구 설명 창의 텍스트의 요약된 버전에 도구 설명의 전체 텍스트를 표시할지 여부를 지정 합니다.  
  
```  
void EnableFullTextTooltip(BOOL bOn=TRUE);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `bOn`  
 `TRUE`모든 텍스트를 표시 하려면 `FALSE` 텍스트 표시할 잘립니다.  
  
### <a name="remarks"></a>주의  
  
##  <a name="enablemenufont"></a>CMFCButton::EnableMenuFont  
 단추 텍스트 글꼴을 응용 프로그램 메뉴 글꼴로 같은지 여부를 지정 합니다.  
  
```  
void EnableMenuFont(
    BOOL bOn=TRUE,  
    BOOL bRedraw=TRUE);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `bOn`  
 `TRUE`단추 텍스트 글꼴;로 응용 프로그램 메뉴 글꼴을 사용 하려면 `FALSE` 시스템 글꼴 크기를 사용 합니다. 기본값은 `TRUE`입니다.  
  
 [in] `bRedraw`  
 `TRUE`화면을 즉시 다시 그리게 그렇지 않으면 `FALSE`합니다. 기본값은 `TRUE`입니다.  
  
### <a name="remarks"></a>주의  
 단추 텍스트 글꼴을 지정 하려면이 메서드를 사용 하지 않는 경우에 있는 글꼴을 지정할 수 있습니다는 [CWnd::SetFont](../../mfc/reference/cwnd-class.md#setfont) 메서드. 글꼴을 전혀 지정 하지 않으면 기본 글꼴을 설정 하는 프레임 워크입니다.  
  
##  <a name="enablewindowstheming"></a>CMFCButton::EnableWindowsTheming  
 단추 테두리의 스타일은 현재 Windows 테마에 해당 하는지 여부를 지정 합니다.  
  
```  
static void EnableWindowsTheming(BOOL bEnable = TRUE);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `bEnable`  
 `TRUE`현재 Windows 테마를 그리는 데 사용할 단추 테두리입니다. `FALSE` Windows 테마를 사용 하지 않도록 합니다. 기본값은 `TRUE`입니다.  
  
### <a name="remarks"></a>주의  
 이 메서드에서 파생 되는 응용 프로그램의 모든 단추에 영향을 줍니다는 `CMFCButton` 클래스입니다.  
  
##  <a name="gettooltipctrl"></a>CMFCButton::GetToolTipCtrl  
 기본 도구 설명 컨트롤에 대 한 참조를 반환합니다.  
  
```  
CToolTipCtrl& GetToolTipCtrl();
```  
  
### <a name="return-value"></a>반환 값  
 기본 도구 설명 컨트롤에 대 한 참조입니다.  
  
### <a name="remarks"></a>주의  
  
##  <a name="isautocheck"></a>CMFCButton::IsAutoCheck  
 확인란 또는 라디오 단추는 자동 단추 인지를 나타냅니다.  
  
```  
BOOL IsAutoCheck() const;  
```  
  
### <a name="return-value"></a>반환 값  
 `TRUE`단추에 스타일 BS_AUTOCHECKBOX 또는 BS_AUTORADIOBUTTON; 그렇지 않으면 `FALSE`합니다.  
  
### <a name="remarks"></a>주의  
  
##  <a name="isautorepeatcommandmode"></a>CMFCButton::IsAutorepeatCommandMode  
 단추 자동 반복 모드로 설정 되어 있는지 여부를 나타냅니다.  
  
```  
BOOL IsAutorepeatCommandMode() const;  
```  
  
### <a name="return-value"></a>반환 값  
 단추 자동 반복 모드;로 설정 되어 있으면 TRUE입니다. 그렇지 않으면 FALSE입니다.  
  
### <a name="remarks"></a>주의  
 사용 된 [CMFCButton::SetAutorepeatMode](#setautorepeatmode) 단추를 자동 반복 모드로 설정 하는 방법입니다.  
  
##  <a name="ischeckbox"></a>CMFCButton::IsCheckBox  
 단추 확인란 단추 인지를 나타냅니다.  
  
```  
BOOL IsCheckBox() const;  
```  
  
### <a name="return-value"></a>반환 값  
 TRUE 이면 단추에 BS_CHECKBOX 또는 BS_AUTOCHECKBOX 스타일입니다. 그렇지 않으면 FALSE입니다.  
  
### <a name="remarks"></a>주의  
  
##  <a name="ischecked"></a>CMFCButton::IsChecked  
 현재 단추가 선택 되어 있는지를 나타냅니다.  
  
```  
BOOL IsChecked() const;  
```  
  
### <a name="return-value"></a>반환 값  
 `TRUE`현재 단추가 선택 되는 경우 그렇지 않으면 `FALSE`합니다.  
  
### <a name="remarks"></a>주의  
 프레임 워크에서는 다양 한 방법 다양 한 종류의 단추 체크 되었음을 나타냅니다. 예, 라디오 단추를 검사 점;이 포함 된 경우 포함 된 경우에 확인란이 선택 되어 있는 **X**합니다.  
  
##  <a name="ishighlighted"></a>CMFCButton::IsHighlighted  
 단추가 강조 표시 하는지 여부를 나타냅니다.  
  
```  
BOOL IsHighlighted() const;  
```  
  
### <a name="return-value"></a>반환 값  
 TRUE 이면 단추가 강조 표시 됩니다. 그렇지 않으면 FALSE입니다.  
  
### <a name="remarks"></a>주의  
 단추에는 단추 위로 마우스를 가져가면 강조 표시 됩니다.  
  
##  <a name="ispressed"></a>CMFCButton::IsPressed  
 단추 푸시되는 강조 표시 된 지를 나타냅니다.  
  
```  
BOOL IsPressed() const;  
```  
  
### <a name="return-value"></a>반환 값  
 TRUE 이면 다음을 추가 합니다. 그렇지 않으면 FALSE입니다.  
  
### <a name="remarks"></a>주의  
  
##  <a name="ispushed"></a>CMFCButton::IsPushed  
 단추를 누를 있는지 여부를 나타냅니다.  
  
```  
BOOL IsPushed() const;  
```  
  
### <a name="return-value"></a>반환 값  
 TRUE 이면에서는 단추를 누를 수 있습니다. 그렇지 않으면 FALSE입니다.  
  
### <a name="remarks"></a>주의  
  
##  <a name="isradiobutton"></a>CMFCButton::IsRadioButton  
 단추는 라디오 단추 인지를 나타냅니다.  
  
```  
BOOL IsRadioButton() const;  
```  
  
### <a name="return-value"></a>반환 값  
 TRUE 이면 단추 스타일은 BS_RADIOBUTTON 이나 BS_AUTORADIOBUTTON; 그렇지 않으면 FALSE입니다.  
  
### <a name="remarks"></a>주의  
  
##  <a name="iswindowsthemingenabled"></a>CMFCButton::IsWindowsThemingEnabled  
 단추 테두리의 스타일은 현재 Windows 테마에 해당 하는지 여부를 나타냅니다.  
  
```  
static BOOL IsWindowsThemingEnabled();
```  
  
### <a name="return-value"></a>반환 값  
 `TRUE`단추 테두리의 스타일은 현재 Windows 테마;에 해당 하는 경우 그렇지 않으면 `FALSE`합니다.  
  
##  <a name="m_bdrawfocus"></a>CMFCButton::m_bDrawFocus  
 단추 주위에 포커스 영역을 그릴 것인지를 나타냅니다.  
  
```  
BOOL m_bDrawFocus;  
```  
  
### <a name="remarks"></a>주의  
 설정의 `m_bDrawFocus` 멤버를 `TRUE` 프레임 워크 단추의 텍스트 주위에 포커스 영역을 그리는 단추 포커스를 받을 경우 이미지는 않도록 지정 하려면.  
  
 `CMFCButton` 생성자에이 멤버를 초기화 합니다. `TRUE`합니다.  
  
##  <a name="m_bhighlightchecked"></a>CMFCButton::m_bHighlightChecked  
 커서를 위로 이동할 때 BS_CHECKBOX 스타일 단추를 강조 표시 여부를 나타냅니다.  
  
```  
BOOL m_bHighlightChecked;  
```  
  
### <a name="remarks"></a>주의  
 설정의 `m_bHighlightChecked` 멤버를 `TRUE` 위로 마우스를 가져가면 프레임 워크 BS_CHECKBOX 스타일 단추가 강조 표시 되어 지정할 수 있습니다.  
  
##  <a name="m_brightimage"></a>CMFCButton::m_bRightImage  
 단추 오른쪽에 이미지를 표시할지 여부를 나타냅니다.  
  
```  
BOOL m_bRightImage;  
```  
  
### <a name="remarks"></a>주의  
 설정의 `m_bRightImage` 멤버를 `TRUE` 프레임 워크는 단추의 텍스트 레이블 오른쪽에는 단추 이미지에 표시 되도록 지정할에 있습니다.  
  
##  <a name="m_btransparent"></a>CMFCButton::m_bTransparent  
 단추 투명 한지 여부를 나타냅니다.  
  
```  
BOOL m_bTransparent;  
```  
  
### <a name="remarks"></a>주의  
 설정의 `m_bTransparent` 멤버를 `TRUE` 는 프레임 워크는 투명 하 게 단추를 지정 합니다. `CMFCButton` 생성자에이 멤버를 초기화 합니다. `FALSE`합니다.  
  
##  <a name="m_nalignstyle"></a>CMFCButton::m_nAlignStyle  
 단추 텍스트의 맞춤을 지정 합니다.  
  
```  
AlignStyle m_nAlignStyle;  
```  
  
### <a name="remarks"></a>주의  
 다음 중 하나를 사용 하 여 `CMFCButton::AlignStyle` 단추 텍스트의 맞춤을 지정 하는 열거형 값:  
  
|값|설명|  
|-----------|-----------------|  
|ALIGN_CENTER|(기본값) 단추 텍스트를 단추의 가운데에 맞춥니다.|  
|ALIGN_LEFT|단추 텍스트를 단추 왼쪽에 맞춥니다.|  
|ALIGN_RIGHT|단추 텍스트를 단추의 오른쪽에 맞춥니다.|  
  
 `CMFCButton` 생성자 ALIGN_CENTER에이 멤버를 초기화 합니다.  
  
##  <a name="m_nflatstyle"></a>CMFCButton::m_nFlatStyle  
 예: 여백, 플랫 형식의 세미콜론 평면 또는 3D 단추 스타일을 지정합니다.  
  
```  
FlatStyle  m_nFlatStyle;  
```  
  
### <a name="remarks"></a>주의  
 다음 표에 `CMFCButton::m_nFlatStyle` 단추의 모양을 지정 하는 열거형 값입니다.  
  
|값|설명|  
|-----------|-----------------|  
|BUTTONSTYLE_3D|(기본값) 에 높음,&3; 차원 면에는 단추가 나타납니다. 단추를 클릭 하 고, 심층 들여쓰기에 눌러야 하는 단추가 나타납니다.|  
|BUTTONSTYLE_FLAT|마우스 단추 위로 일시 중지 하지 않습니다 단추&2; 차원 수에 나타나고 볼록한 쪽에는 없습니다. 단추 위로 마우스를 놓을 때에 낮음,&3; 차원 면에는 단추가 나타납니다. 단추를 클릭 하 고, 단순 들여쓰기에 눌러야 하는 단추가 나타납니다.|  
|BUTTONSTYLE_SEMIFLAT|이 단추는 낮음,&3; 차원 면에 나타납니다. 단추를 클릭 하 고, 심층 들여쓰기에 눌러야 하는 단추가 나타납니다.|  
|BUTTONSTYLE_NOBORDERS|단추 발생 못한지 않습니다 양쪽와 항상&2; 차원를 표시 합니다. 단추를 클릭할 때 들여쓰기에 누를 나타나지 않습니다.|  
  
 `CMFCButton` 생성자에이 멤버를 초기화 합니다. `BUTTONSTYLE_3D`합니다.  
  
### <a name="example"></a>예제  
 다음 예제에서는 값을 설정 하는 방법의 `m_nFlatStyle` 에서 멤버 변수는 `CMFCButton` 클래스입니다. 이 예제는의 일부는 [새 컨트롤 샘플](../../visual-cpp-samples.md)합니다.  
  
 [!code-cpp[NVC_MFC_NewControls #&28;](../../mfc/reference/codesnippet/cpp/cmfcbutton-class_1.h)]  
[!code-cpp[NVC_MFC_NewControls #&29;](../../mfc/reference/codesnippet/cpp/cmfcbutton-class_5.cpp)]  
  
##  <a name="ondraw"></a>CMFCButton::OnDraw  
 단추를 그리는 프레임 워크에 의해 호출 됩니다.  
  
```  
virtual void OnDraw(
    CDC* pDC,  
    const CRect& rect,  
    UINT uiState);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `pDC`  
 장치 컨텍스트에 대한 포인터입니다.  
  
 [in] `rect`  
 단추를 제한 하는 사각형에 대 한 참조입니다.  
  
 [in] `uiState`  
 현재 단추 상태입니다. 자세한 내용은 참조는 `itemState` 의 멤버는 [DRAWITEMSTRUCT 구조체](../../mfc/reference/drawitemstruct-structure.md) 항목입니다.  
  
### <a name="remarks"></a>주의  
 단추를 그리는 사용자 고유의 코드를 사용 하 여이 메서드를 재정의 합니다.  
  
##  <a name="ondrawborder"></a>CMFCButton::OnDrawBorder  
 단추의 테두리를 그리는 프레임 워크에 의해 호출 됩니다.  
  
```  
virtual void OnDrawBorder(
    CDC* pDC,  
    CRect& rectClient,  
    UINT uiState);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `pDC`  
 장치 컨텍스트에 대한 포인터입니다.  
  
 [in] `rectClient`  
 단추를 제한 하는 사각형에 대 한 참조입니다.  
  
 [in] `uiState`  
 현재 단추 상태입니다. 자세한 내용은 참조는 `itemState` 의 멤버는 [DRAWITEMSTRUCT 구조체](../../mfc/reference/drawitemstruct-structure.md) 항목입니다.  
  
### <a name="remarks"></a>주의  
 테두리를 그리는 사용자 고유의 코드를 사용 하 여이 메서드를 재정의 합니다.  
  
##  <a name="ondrawfocusrect"></a>CMFCButton::OnDrawFocusRect  
 단추에 대 한 포커스 사각형을 그리는 프레임 워크에 의해 호출 됩니다.  
  
```  
virtual void OnDrawFocusRect(
    CDC* pDC,  
    const CRect& rectClient);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `pDC`  
 장치 컨텍스트에 대한 포인터입니다.  
  
 [in] `rectClient`  
 단추를 제한 하는 사각형에 대 한 참조입니다.  
  
### <a name="remarks"></a>주의  
 포커스 사각형을 그리는 사용자 고유의 코드를 사용 하 여이 메서드를 재정의 합니다.  
  
##  <a name="ondrawtext"></a>CMFCButton::OnDrawText  
 단추 텍스트를 그릴 프레임 워크에 의해 호출 됩니다.  
  
```  
virtual void OnDrawText(
    CDC* pDC,  
    const CRect& rect,  
    const CString& strText,  
    UINT uiDTFlags,  
    UINT uiState);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `pDC`  
 장치 컨텍스트에 대한 포인터입니다.  
  
 [in] `rect`  
 단추를 제한 하는 사각형에 대 한 참조입니다.  
  
 [in] `strText`  
 그릴 텍스트입니다.  
  
 [in] `uiDTFlags`  
 텍스트의 서식을 지정 하는 방법을 지정 하는 플래그입니다. 자세한 내용은 참조는 `nFormat` 의 매개 변수는 [CDC::DrawText](../../mfc/reference/cdc-class.md#drawtext) 메서드.  
  
 [in] `uiState`  
 (예약 됨.)  
  
### <a name="remarks"></a>주의  
 단추 텍스트를 그릴 사용자 고유의 코드를 사용 하 여이 메서드를 재정의 합니다.  
  
##  <a name="onfillbackground"></a>CMFCButton::OnFillBackground  
 단추 텍스트의 배경을 그리기 위한 프레임 워크에 의해 호출 됩니다.  
  
```  
virtual void OnFillBackground(
    CDC* pDC,  
    const CRect& rectClient);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `pDC`  
 장치 컨텍스트에 대한 포인터입니다.  
  
 [in] `rectClient`  
 단추를 제한 하는 사각형에 대 한 참조입니다.  
  
### <a name="remarks"></a>주의  
 단추의 배경을 그리기 위한 사용자 고유의 코드를 사용 하 여이 메서드를 재정의 합니다.  
  
##  <a name="selectfont"></a>CMFCButton::SelectFont  
 지정된 된 장치 컨텍스트에 연결 되는 글꼴을 가져옵니다.  
  
```  
virtual CFont* SelectFont(CDC* pDC);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `pDC`  
 장치 컨텍스트에 대한 포인터입니다.  
  
### <a name="return-value"></a>반환 값  
 사용자 고유의 코드를 사용 하 여 글꼴을 검색 하려면이 메서드를 재정의 합니다.  
  
### <a name="remarks"></a>주의  
  
##  <a name="setautorepeatmode"></a>CMFCButton::SetAutorepeatMode  
 단추 자동 반복 모드를 설정합니다.  
  
```  
void SetAutorepeatMode(int nTimeDelay=500);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `nTimeDelay`  
 부모 창에 전송 된 메시지를 사이의 간격을 지정 하는 음수가 아닌 숫자. 기본값은 500 밀리초 하는 간격 밀리초 단위로 측정 됩니다. 자동 반복 메시지 모드를 사용 하지 않도록 설정 하려면&0;을 지정 합니다.  
  
### <a name="remarks"></a>주의  
 이 메서드를 사용 하면 지속적으로 메시지를 보내는 WM_COMMAND 부모 창에 단추를 놓을 때까지 단추 또는 `nTimeDelay` 매개 변수는&0;으로 설정 됩니다.  
  
##  <a name="setcheckedimage"></a>CMFCButton::SetCheckedImage  
 이미지 선택된 단추를 설정합니다.  
  
```  
void SetCheckedImage(
    HICON hIcon,  
    BOOL bAutoDestroy=TRUE,  
    HICON hIconHot=NULL,  
    HICON hIconDisabled=NULL,  
    BOOL bAlphaBlend=FALSE);

 
void SetCheckedImage(
    HBITMAP hBitmap,  
    BOOL bAutoDestroy=TRUE,  
    HBITMAP hBitmapHot=NULL,  
    BOOL bMap3dColors=TRUE,  
    HBITMAP hBitmapDisabled=NULL);

 
void SetCheckedImage(
    UINT uiBmpResId,  
    UINT uiBmpHotResId=0,  
    UINT uiBmpDsblResID=0);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `hIcon`  
 비트맵 및 새 이미지에 대 한 마스크를 포함 하는 아이콘에 대 한 핸들입니다.  
  
 [in] `bAutoDestroy`  
 `TRUE`비트맵 리소스를 자동으로 소멸 될 있는지를 지정 하려면 그렇지 않으면 `FALSE`합니다. 기본값은 `TRUE`입니다.  
  
 [in] `hIconHot`  
 선택된 된 상태에 대 한 이미지를 포함 하는 아이콘에 대 한 핸들입니다.  
  
 [in] `hBitmap`  
 선택 되지 않은 상태에 대 한 이미지를 포함 하는 비트맵 핸들입니다.  
  
 [in] `hBitmapHot`  
 선택된 된 상태에 대 한 이미지를 포함 하는 비트맵 핸들입니다.  
  
 [in] `bMap3dColors`  
 단추 배경;에 대 한 투명 한 색을 지정합니다. 즉, 단추 모양을 합니다. `TRUE`(192, 192, 192); RGB 색상 값을 사용 하려면 `FALSE` 에 정의 된 색 값을 사용 하 여 `AFX_GLOBAL_DATA::clrBtnFace`합니다.  
  
 [in] `uiBmpResId`  
 선택 되지 않은 이미지에 대 한 리소스 ID입니다.  
  
 [in] `uiBmpHotResId`  
 선택한 이미지에 대 한 리소스 ID입니다.  
  
 [in] `hIconDisabled`  
 사용 하지 않는 이미지에 대 한 아이콘에 대 한 핸들입니다.  
  
 [in] `hBitmapDisabled`  
 비활성화 된 이미지가 포함 된 비트맵에 대 한 핸들입니다.  
  
 [in] `uiBmpDsblResID`  
 비활성화 된 비트맵의 리소스 ID입니다.  
  
 [in] `bAlphaBlend`  
 `TRUE`알파 채널;를 사용 하는 유일한 32 비트 이미지를 사용 하려면 `FALSE`, 알파 채널 이미지만 사용 하지 않도록 합니다. 기본값은 `FALSE`입니다.  
  
### <a name="remarks"></a>주의  
  
##  <a name="setfacecolor"></a>CMFCButton::SetFaceColor  
 단추 텍스트의 배경색을 설정합니다.  
  
```  
void SetFaceColor(
    COLORREF crFace,  
    BOOL bRedraw=TRUE);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `crFace`  
 RGB 색상 값입니다.  
  
 [in] `bRedraw`  
 `TRUE`화면을 즉시 다시 그리게 그렇지 않으면 `FALSE`합니다.  
  
### <a name="remarks"></a>주의  
 단추 배경 (면)에 대 한 새 채우기 색을 정의 하려면이 메서드를 사용 합니다. 백그라운드 하지 않습니다 채워진 경우는 [CMFCButton::m_bTransparent](#m_btransparent) 멤버 변수는 `TRUE`합니다.  
  
##  <a name="setimage"></a>CMFCButton::SetImage  
 단추에 대 한 이미지를 설정합니다.  
  
```  
void SetImage(
    HICON hIcon,  
    BOOL bAutoDestroy=TRUE,  
    HICON hIconHot=NULL,  
    HICON hIconDisabled=NULL,  
    BOOL bAlphaBlend=FALSE);

 
void SetImage(
    HBITMAP hBitmap,  
    BOOL bAutoDestroy=TRUE,  
    HBITMAP hBitmapHot=NULL,  
    BOOL bMap3dColors=TRUE,  
    HBITMAP hBitmapDisabled=NULL);

 
void SetImage(
    UINT uiBmpResId,  
    UINT uiBmpHotResId=0,  
    UINT uiBmpDsblResID=0);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `hIcon`  
 비트맵 및 새 이미지에 대 한 마스크를 포함 하는 아이콘에 대 한 핸들입니다.  
  
 [in] `bAutoDestroy`  
 `TRUE`비트맵 리소스를 자동으로 소멸 될 있는지를 지정 하려면 그렇지 않으면 `FALSE`합니다. 기본값은 `TRUE`입니다.  
  
 [in] `hIconHot`  
 선택된 된 상태에 대 한 이미지를 포함 하는 아이콘에 대 한 핸들입니다.  
  
 [in] `hBitmap`  
 선택 되지 않은 상태에 대 한 이미지를 포함 하는 비트맵 핸들입니다.  
  
 [in] `hBitmapHot`  
 선택된 된 상태에 대 한 이미지를 포함 하는 비트맵 핸들입니다.  
  
 [in] `uiBmpResId`  
 선택 되지 않은 이미지에 대 한 리소스 ID입니다.  
  
 [in] `uiBmpHotResId`  
 선택한 이미지에 대 한 리소스 ID입니다.  
  
 [in] `bMap3dColors`  
 단추 배경;에 대 한 투명 한 색을 지정합니다. 즉, 단추 모양을 합니다. `TRUE`(192, 192, 192); RGB 색상 값을 사용 하려면 `FALSE` 에 정의 된 색 값을 사용 하 여 `AFX_GLOBAL_DATA::clrBtnFace`합니다.  
  
 [in] `hIconDisabled`  
 사용 하지 않는 이미지에 대 한 아이콘에 대 한 핸들입니다.  
  
 [in] `hBitmapDisabled`  
 비활성화 된 이미지가 포함 된 비트맵에 대 한 핸들입니다.  
  
 [in] `uiBmpDsblResID`  
 비활성화 된 비트맵의 리소스 ID입니다.  
  
 [in] `bAlphaBlend`  
 `TRUE`알파 채널;를 사용 하는 유일한 32 비트 이미지를 사용 하려면 `FALSE`, 알파 채널 이미지만 사용 하지 않도록 합니다. 기본값은 `FALSE`입니다.  
  
### <a name="remarks"></a>주의  
  
### <a name="example"></a>예제  
 다음 예제에는 다양 한 버전을 사용 하는 방법을 보여 줍니다는 `SetImage` 에서 메서드는 `CMFCButton` 클래스입니다. 일부인이 예제는 [새 컨트롤 샘플](../../visual-cpp-samples.md)합니다.  
  
 [!code-cpp[NVC_MFC_NewControls #&28;](../../mfc/reference/codesnippet/cpp/cmfcbutton-class_1.h)]  
[!code-cpp[NVC_MFC_NewControls #&31;](../../mfc/reference/codesnippet/cpp/cmfcbutton-class_2.cpp)]  
  
##  <a name="setmousecursor"></a>CMFCButton::SetMouseCursor  
 커서 이미지를 설정합니다.  
  
```  
void SetMouseCursor(HCURSOR hcursor);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `hcursor`  
 커서의 핸들입니다.  
  
### <a name="remarks"></a>주의  
 단추와 손 모양 커서 등 커서 이미지를 연결 하려면이 메서드를 사용 합니다. 커서는 응용 프로그램 리소스에서 로드 됩니다.  
  
### <a name="example"></a>예제  
 다음 예제에 사용 하는 방법을 보여 줍니다는 `SetMouseCursor` 에서 메서드는 `CMFCButton` 클래스입니다. 이 예제에서 코드의 일부인는 [새 컨트롤 샘플](../../visual-cpp-samples.md)합니다.  
  
 [!code-cpp[NVC_MFC_NewControls #&28;](../../mfc/reference/codesnippet/cpp/cmfcbutton-class_1.h)]  
[!code-cpp[NVC_MFC_NewControls #&30;](../../mfc/reference/codesnippet/cpp/cmfcbutton-class_6.cpp)]  
  
##  <a name="setmousecursorhand"></a>CMFCButton::SetMouseCursorHand  
 손 모양 이미지에 커서를 설정합니다.  
  
```  
void SetMouseCursorHand();
```  
  
### <a name="remarks"></a>주의  
 손 모양 커서 이미지 단추와 연결 하려면이 메서드를 사용 합니다. 커서는 응용 프로그램 리소스에서 로드 됩니다.  
  
##  <a name="setstdimage"></a>CMFCButton::SetStdImage  
 사용 하 여 한 `CMenuImages` 단추 이미지를 설정 하는 개체입니다.  
  
```  
void SetStdImage(
    CMenuImages::IMAGES_IDS id,  
    CMenuImages::IMAGE_STATE state=CMenuImages::ImageBlack,  
    CMenuImages::IMAGES_IDS idDisabled=(CMenuImages::IMAGES_IDS)0);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `id`  
 에 정의 되어 있는 단추 이미지 식별자 중 하나는 `CMenuImage::IMAGES_IDS` 열거형입니다. 이미지 값 화살표, 핀 및 라디오 단추와 같은 이미지를 지정합니다.  
  
 [in] `state`  
 에 정의 되어 있는 단추 이미지 상태 식별자 중 하나는 `CMenuImages::IMAGE_STATE` 열거형입니다. 이미지 상태로 검정, 회색, 밝은 회색 흰색 및 어두운 회색 예: 단추 색을 지정 합니다. 기본값은 `CMenuImages::ImageBlack`입니다.  
  
 [in] `idDisabled`  
 에 정의 되어 있는 단추 이미지 식별자 중 하나는 `CMenuImage::IMAGES_IDS` 열거형입니다. 이미지 단추는 비활성화 하는 것을 나타냅니다. 기본값은 첫 번째 단추 이미지 ( `CMenuImages::IdArrowDown`).  
  
### <a name="remarks"></a>주의  
  
##  <a name="settextcolor"></a>CMFCButton::SetTextColor  
 선택 되지 않은 단추에 대 한 단추 텍스트의 색을 설정 합니다.  
  
```  
void SetTextColor(COLORREF clrText);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `clrText`  
 RGB 색상 값입니다.  
  
### <a name="remarks"></a>주의  
  
##  <a name="settexthotcolor"></a>CMFCButton::SetTextHotColor  
 선택 된 단추에 대 한 단추 텍스트의 색을 설정 합니다.  
  
```  
void SetTextHotColor(COLORREF clrTextHot);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `clrTextHot`  
 RGB 색상 값입니다.  
  
### <a name="remarks"></a>주의  
  
##  <a name="settooltip"></a>CMFCButton::SetTooltip  
 단추를 도구 설명에 연결합니다.  
  
```  
void SetTooltip(LPCTSTR lpszToolTipText);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `lpszToolTipText`  
 도구 설명에 표시할 텍스트에 대 한 포인터입니다. 도구 설명을 사용 하지 않도록 설정 하려면 NULL을 지정 합니다.  
  
### <a name="remarks"></a>주의  
  
##  <a name="sizetocontent"></a>CMFCButton::SizeToContent  
 단추 텍스트와 이미지를 포함 하는 단추 크기가 조정 됩니다.  
  
```  
virtual CSize SizeToContent(BOOL bCalcOnly=FALSE);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `bCalcOnly`  
 `TRUE`을 계산 하지만 변경 하지 단추;의 새 크기를 `FALSE` 단추의 크기를 변경 합니다. 기본값은 `FALSE`입니다.  
  
### <a name="return-value"></a>반환 값  
 A `CSize` 버튼의 새 크기를 포함 하는 개체입니다.  
  
### <a name="remarks"></a>주의  
 이 메서드는 기본적으로 10 픽셀의 가로 여백 및 여백이 5 픽셀의 포함 된 새 크기를 계산 합니다.  
  
## <a name="see-also"></a>참고 항목  
 [계층 구조 차트](../../mfc/hierarchy-chart.md)   
 [클래스](../../mfc/reference/mfc-classes.md)   
 [CMFCLinkCtrl 클래스](../../mfc/reference/cmfclinkctrl-class.md)   
 [CMFCColorButton 클래스](../../mfc/reference/cmfccolorbutton-class.md)   
 [CMFCMenuButton 클래스](../../mfc/reference/cmfcmenubutton-class.md)
