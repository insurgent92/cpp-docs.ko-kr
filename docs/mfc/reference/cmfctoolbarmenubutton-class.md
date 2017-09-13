---
title: "CMFCToolBarMenuButton 클래스 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- CMFCToolBarMenuButton
- AFXTOOLBARMENUBUTTON/CMFCToolBarMenuButton
- AFXTOOLBARMENUBUTTON/CMFCToolBarMenuButton::CMFCToolBarMenuButton
- AFXTOOLBARMENUBUTTON/CMFCToolBarMenuButton::CompareWith
- AFXTOOLBARMENUBUTTON/CMFCToolBarMenuButton::CopyFrom
- AFXTOOLBARMENUBUTTON/CMFCToolBarMenuButton::CreateFromMenu
- AFXTOOLBARMENUBUTTON/CMFCToolBarMenuButton::CreateMenu
- AFXTOOLBARMENUBUTTON/CMFCToolBarMenuButton::CreatePopupMenu
- AFXTOOLBARMENUBUTTON/CMFCToolBarMenuButton::EnableQuickCustomize
- AFXTOOLBARMENUBUTTON/CMFCToolBarMenuButton::GetCommands
- AFXTOOLBARMENUBUTTON/CMFCToolBarMenuButton::GetImageRect
- AFXTOOLBARMENUBUTTON/CMFCToolBarMenuButton::GetPaletteRows
- AFXTOOLBARMENUBUTTON/CMFCToolBarMenuButton::GetPopupMenu
- AFXTOOLBARMENUBUTTON/CMFCToolBarMenuButton::HasButton
- AFXTOOLBARMENUBUTTON/CMFCToolBarMenuButton::HaveHotBorder
- AFXTOOLBARMENUBUTTON/CMFCToolBarMenuButton::IsBorder
- AFXTOOLBARMENUBUTTON/CMFCToolBarMenuButton::IsClickedOnMenu
- AFXTOOLBARMENUBUTTON/CMFCToolBarMenuButton::IsDroppedDown
- AFXTOOLBARMENUBUTTON/CMFCToolBarMenuButton::IsEmptyMenuAllowed
- AFXTOOLBARMENUBUTTON/CMFCToolBarMenuButton::IsExclusive
- AFXTOOLBARMENUBUTTON/CMFCToolBarMenuButton::IsMenuPaletteMode
- AFXTOOLBARMENUBUTTON/CMFCToolBarMenuButton::IsQuickMode
- AFXTOOLBARMENUBUTTON/CMFCToolBarMenuButton::IsTearOffMenu
- AFXTOOLBARMENUBUTTON/CMFCToolBarMenuButton::OnAfterCreatePopupMenu
- AFXTOOLBARMENUBUTTON/CMFCToolBarMenuButton::OnBeforeDrag
- AFXTOOLBARMENUBUTTON/CMFCToolBarMenuButton::OnCalculateSize
- AFXTOOLBARMENUBUTTON/CMFCToolBarMenuButton::OnCancelMode
- AFXTOOLBARMENUBUTTON/CMFCToolBarMenuButton::OnChangeParentWnd
- AFXTOOLBARMENUBUTTON/CMFCToolBarMenuButton::OnClick
- AFXTOOLBARMENUBUTTON/CMFCToolBarMenuButton::OnClickMenuItem
- AFXTOOLBARMENUBUTTON/CMFCToolBarMenuButton::OnContextHelp
- AFXTOOLBARMENUBUTTON/CMFCToolBarMenuButton::OnDraw
- AFXTOOLBARMENUBUTTON/CMFCToolBarMenuButton::OnDrawOnCustomizeList
- AFXTOOLBARMENUBUTTON/CMFCToolBarMenuButton::OpenPopupMenu
- AFXTOOLBARMENUBUTTON/CMFCToolBarMenuButton::ResetImageToDefault
- AFXTOOLBARMENUBUTTON/CMFCToolBarMenuButton::SaveBarState
- AFXTOOLBARMENUBUTTON/CMFCToolBarMenuButton::Serialize
- AFXTOOLBARMENUBUTTON/CMFCToolBarMenuButton::SetACCData
- AFXTOOLBARMENUBUTTON/CMFCToolBarMenuButton::SetMenuOnly
- AFXTOOLBARMENUBUTTON/CMFCToolBarMenuButton::SetMenuPaletteMode
- AFXTOOLBARMENUBUTTON/CMFCToolBarMenuButton::SetMessageWnd
- AFXTOOLBARMENUBUTTON/CMFCToolBarMenuButton::SetRadio
- AFXTOOLBARMENUBUTTON/CMFCToolBarMenuButton::SetTearOff
- AFXTOOLBARMENUBUTTON/CMFCToolBarMenuButton::DrawDocumentIcon
- AFXTOOLBARMENUBUTTON/CMFCToolBarMenuButton::m_bAlwaysCallOwnerDraw
dev_langs:
- C++
helpviewer_keywords:
- CMFCToolBarMenuButton class
ms.assetid: cfa50176-7e4b-4527-9904-86a1b48fc1bc
caps.latest.revision: 31
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
ms.openlocfilehash: a06fd323862c6869463b4db0977816b5707c3e18
ms.contentlocale: ko-kr
ms.lasthandoff: 02/24/2017

---
# <a name="cmfctoolbarmenubutton-class"></a>CMFCToolBarMenuButton 클래스
팝업 메뉴를 포함하는 도구 모음 단추입니다.  
 [!INCLUDE[cpp_fp_under_construction](../../mfc/reference/includes/cpp_fp_under_construction_md.md)]  
  
## <a name="syntax"></a>구문  
  
```  
class CMFCToolBarMenuButton : public CMFCToolBarButton  
```  
  
## <a name="members"></a>멤버  
  
### <a name="public-constructors"></a>Public 생성자  
  
|이름|설명|  
|----------|-----------------|  
|[CMFCToolBarMenuButton::CMFCToolBarMenuButton](#cmfctoolbarmenubutton)|`CMFCToolBarMenuButton` 개체를 생성합니다.|  
  
### <a name="public-methods"></a>Public 메서드  
  
|이름|설명|  
|----------|-----------------|  
|[CMFCToolBarMenuButton::CompareWith](#comparewith)|이 인스턴스를 제공 된 `CMFCToolBarButton` 개체입니다. (재정의 [CMFCToolBarButton::CompareWith](../../mfc/reference/cmfctoolbarbutton-class.md#comparewith).)|  
|[CMFCToolBarMenuButton::CopyFrom](#copyfrom)|현재 단추에 다른 도구 모음 단추의 속성을 복사합니다. (재정의 [CMFCToolBarButton::CopyFrom](../../mfc/reference/cmfctoolbarbutton-class.md#copyfrom).)|  
|[CMFCToolBarMenuButton::CreateFromMenu](#createfrommenu)|창 메뉴 핸들에서 도구 모음 메뉴를 초기화합니다.|  
|[CMFCToolBarMenuButton::CreateMenu](#createmenu)|도구 모음 메뉴의 명령으로 이루어진 Windows 메뉴를 만듭니다. 창 메뉴에 대 한 핸들을 반환합니다.|  
|[CMFCToolBarMenuButton::CreatePopupMenu](#createpopupmenu)|팝업 메뉴 개체를 만듭니다 ( [CMFCPopupMenu 클래스](../../mfc/reference/cmfcpopupmenu-class.md)) 도구 모음 메뉴를 표시 합니다.|  
|[CMFCToolBarMenuButton::EnableQuickCustomize](#enablequickcustomize)||  
|[CMFCToolBarMenuButton::GetCommands](#getcommands)|도구 모음 메뉴에 있는 명령 목록에 대 한 읽기 전용 액세스를 제공합니다.|  
|[CMFCToolBarMenuButton::GetImageRect](#getimagerect)|단추 이미지에 대 한 경계 사각형을 검색 합니다.|  
|[CMFCToolBarMenuButton::GetPaletteRows](#getpaletterows)|메뉴 팔레트 모드에 있을 때 팝업 메뉴에서 행의 수를 반환 합니다.|  
|[CMFCToolBarMenuButton::GetPopupMenu](#getpopupmenu)|단추와 연결 되는 팝업 메뉴 개체에 대 한 포인터를 반환 합니다.|  
|[CMFCToolBarMenuButton::HasButton](#hasbutton)||  
|[CMFCToolBarMenuButton::HaveHotBorder](#havehotborder)|사용자가 단추를 선택 단추의 테두리 표시 여부를 결정 합니다. (재정의 [CMFCToolBarButton::HaveHotBorder](../../mfc/reference/cmfctoolbarbutton-class.md#havehotborder).)|  
|[CMFCToolBarMenuButton::IsBorder](#isborder)||  
|[CMFCToolBarMenuButton::IsClickedOnMenu](#isclickedonmenu)||  
|[CMFCToolBarMenuButton::IsDroppedDown](#isdroppeddown)|팝업 메뉴를 표시할지 여부를 결정 합니다.|  
|[CMFCToolBarMenuButton::IsEmptyMenuAllowed](#isemptymenuallowed)|사용자 선택된 된 메뉴 항목에서 하위 메뉴를 열 수 있는지 여부를 결정 하는 프레임 워크에서 호출 됩니다.|  
|[CMFCToolBarMenuButton::IsExclusive](#isexclusive)|단추 인지 단독 모드, 즉 여부 팝업 메뉴에도 계속 열려 다른 도구 모음이 나 단추 위로 포인터를 이동 하는 경우에 결정 합니다.|  
|[CMFCToolBarMenuButton::IsMenuPaletteMode](#ismenupalettemode)|팝업 메뉴 팔레트 모드 인지 여부를 결정 합니다.|  
|[CMFCToolBarMenuButton::IsQuickMode](#isquickmode)||  
|[CMFCToolBarMenuButton::IsTearOffMenu](#istearoffmenu)|팝업 메뉴에 분리 표시줄이 있는지 여부를 결정 합니다.|  
|[CMFCToolBarMenuButton::OnAfterCreatePopupMenu](#onaftercreatepopupmenu)||  
|[CMFCToolBarMenuButton::OnBeforeDrag](#onbeforedrag)|단추를 놓을 수 있는지 여부를 지정 합니다. (재정의 [CMFCToolBarButton::OnBeforeDrag](../../mfc/reference/cmfctoolbarbutton-class.md#onbeforedrag).)|  
|[CMFCToolBarMenuButton::OnCalculateSize](#oncalculatesize)|지정 된 장치 컨텍스트와 도킹 상태에 대 한 단추의 크기를 계산 하는 프레임 워크에서 호출 됩니다. (재정의 [CMFCToolBarButton::OnCalculateSize](../../mfc/reference/cmfctoolbarbutton-class.md#oncalculatesize).)|  
|[CMFCToolBarMenuButton::OnCancelMode](#oncancelmode)|처리 하는 프레임 워크에서 호출 된 [WM_CANCELMODE](http://msdn.microsoft.com/library/windows/desktop/ms632615) 메시지입니다. (재정의 [CMFCToolBarButton::OnCancelMode](../../mfc/reference/cmfctoolbarbutton-class.md#oncancelmode).)|  
|[CMFCToolBarMenuButton::OnChangeParentWnd](#onchangeparentwnd)|새 도구 모음 단추를 삽입할 경우에 프레임 워크에서 호출 합니다. (재정의 [CMFCToolBarButton::OnChangeParentWnd](cmfctoolbarbutton-class.md#onchangeparentwnd).)|  
|[CMFCToolBarMenuButton::OnClick](#onclick)|사용자가 마우스 단추를 클릭할 때 프레임 워크에서 호출 합니다. (재정의 [CMFCToolBarButton::OnClick](../../mfc/reference/cmfctoolbarbutton-class.md#onclick).)|  
|[CMFCToolBarMenuButton::OnClickMenuItem](#onclickmenuitem)|팝업 메뉴에서 항목을 선택할 때 프레임 워크에서 호출 합니다.|  
|[CMFCToolBarMenuButton::OnContextHelp](#oncontexthelp)|부모 도구 모음에서 처리 하는 경우에 프레임 워크에서 호출 된 `WM_HELPHITTEST` 메시지입니다. (재정의 [CMFCToolBarButton::OnContextHelp](../../mfc/reference/cmfctoolbarbutton-class.md#oncontexthelp).)|  
|[CMFCToolBarMenuButton::OnDraw](#ondraw)|지정 된 스타일 및 옵션을 사용 하 여 단추를 그리기 위해 프레임 워크에서 호출 됩니다. (재정의 [CMFCToolBarButton::OnDraw](../../mfc/reference/cmfctoolbarbutton-class.md#ondraw).)|  
|[CMFCToolBarMenuButton::OnDrawOnCustomizeList](#ondrawoncustomizelist)|단추를 그리기 위해 프레임 워크에 의해 호출 된 **명령을** 의 창은 **사용자 지정** 대화 상자입니다. (재정의 [CMFCToolBarButton::OnDrawOnCustomizeList](../../mfc/reference/cmfctoolbarbutton-class.md#ondrawoncustomizelist).)|  
|[CMFCToolBarMenuButton::OpenPopupMenu](#openpopupmenu)|사용자가 팝업 메뉴를 열 때에 프레임 워크에서 호출 합니다.|  
|[CMFCToolBarMenuButton::ResetImageToDefault](#resetimagetodefault)|단추와 연결 되는 이미지의 기본값을 설정 합니다. (재정의 [CMFCToolBarButton::ResetImageToDefault](../../mfc/reference/cmfctoolbarbutton-class.md#resetimagetodefault).)|  
|[CMFCToolBarMenuButton::SaveBarState](#savebarstate)|도구 모음 단추의 상태를 저장합니다. (재정의 [CMFCToolBarButton::SaveBarState](../../mfc/reference/cmfctoolbarbutton-class.md#savebarstate).)|  
|[CMFCToolBarMenuButton::Serialize](#serialize)|이 개체는 보관 파일에서 읽거나 보관 파일에 씁니다. (재정의 [CMFCToolBarButton::Serialize](../../mfc/reference/cmfctoolbarbutton-class.md#serialize).)|  
|[CMFCToolBarMenuButton::SetACCData](#setaccdata)|제공 된 정보를 표시 `CAccessibilityData` 도구 모음 단추에서 내게 필요한 옵션 데이터는 개체입니다. (재정의 [CMFCToolBarButton::SetACCData](../../mfc/reference/cmfctoolbarbutton-class.md#setaccdata).)|  
|[CMFCToolBarMenuButton::SetMenuOnly](#setmenuonly)|도구 모음에 단추를 추가할 수 있는지 여부를 지정 합니다.|  
|[CMFCToolBarMenuButton::SetMenuPaletteMode](#setmenupalettemode)|팝업 메뉴 팔레트 모드 인지 여부를 지정 합니다.|  
|[CMFCToolBarMenuButton::SetMessageWnd](#setmessagewnd)||  
|[CMFCToolBarMenuButton::SetRadio](#setradio)|선택 되어 있는지를 나타내는 아이콘을 표시 하려면 도구 모음 메뉴 단추를 강제로 수행 합니다.|  
|[CMFCToolBarMenuButton::SetTearOff](#settearoff)|분리 지정 팝업 메뉴에 대 한 ID를 표시 합니다.|  
  
### <a name="protected-methods"></a>Protected 메서드  
  
|이름|설명|  
|----------|-----------------|  
|[CMFCToolBarMenuButton::DrawDocumentIcon](#drawdocumenticon)|메뉴 단추에 아이콘을 그립니다.|  
  
### <a name="data-members"></a>데이터 멤버  
  
|이름|설명|  
|----------|-----------------|  
|[CMFCToolBarMenuButton::m_bAlwaysCallOwnerDraw](#m_balwayscallownerdraw)|경우 `TRUE`, 프레임 워크를 항상 호출 [CFrameWndEx::OnDrawMenuImage](../../mfc/reference/cframewndex-class.md#ondrawmenuimage) 단추를 그릴 때.|  
  
## <a name="remarks"></a>주의  
 A `CMFCToolBarMenuButton` 메뉴, 하위 메뉴에 있는 메뉴 항목, 명령을 실행 하거나 메뉴를 표시 하는 단추 또는 메뉴에만 표시 하는 단추 표시 될 수 있습니다. 이미지, 텍스트, 메뉴 핸들 등의 매개 변수를 지정 하 여 동작 및 메뉴 단추의 모양을 결정 하 고 명령 생성자에서 단추와 연결 된 ID `CMFCToolbarMenuButton::CMFCToolbarMenuButton`합니다.  
  
 사용자 지정 클래스에서 파생 된 `CMFCToolbarMenuButton` 클래스를 사용 해야는 [DECLARE_SERIAL](run-time-object-model-services.md#declare_serial) 매크로입니다. [DECLARE_DYNCREATE](run-time-object-model-services.md#declare_dyncreate) 매크로 응용 프로그램을 종료 하는 경우 오류를 생성 합니다.  
  
## <a name="example"></a>예제  
 다음 예제에서는 구성 하는 방법을 한 `CMFCToolBarMenuButton` 개체입니다. 코드는 드롭다운 메뉴 팔레트 모드 임을 지정 하 고 사용자가 메뉴 모음에서 메뉴 단추를 끌 때 생성 되 고 분리 모음에 대 한 ID를 지정 하는 방법을 보여 줍니다. 이 코드 조각은의 일부인는 [워드 패드 샘플](../../visual-cpp-samples.md)합니다.  
  
 [!code-cpp[NVC_MFC_WordPad #&10;](../../mfc/reference/codesnippet/cpp/cmfctoolbarmenubutton-class_1.cpp)]  
  
## <a name="inheritance-hierarchy"></a>상속 계층  
 [CObject](cobject-class.md)  
  
 [CMFCToolBarButton](../../mfc/reference/cmfctoolbarbutton-class.md)  
  
 [CMFCToolBarMenuButton](../../mfc/reference/cmfctoolbarmenubutton-class.md)  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** afxtoolbarmenubutton.h  
  
##  <a name="cmfctoolbarmenubutton"></a>CMFCToolBarMenuButton::CMFCToolBarMenuButton  
 `CMFCToolBarMenuButton` 개체를 생성합니다.  
  
```  
CMFCToolBarMenuButton();
CMFCToolBarMenuButton(const CMFCToolBarMenuButton& src);

CMFCToolBarMenuButton(
    UINT uiID,  
    HMENU hMenu,  
    int iImage,  
    LPCTSTR lpszText=NULL,  
    BOOL bUserButton=FALSE);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `src`  
 기존 `CMFCToolBarMenuButton` 이에 복사 될 개체 `CMFCToolBarMenuButton` 개체입니다.  
  
 [in] `uiID`  
 단추를 클릭할 때 실행할 명령의 ID 또는 ( `UINT`) 명령을 직접 실행 되지 않는 메뉴 단추에 대 한-1입니다.  
  
 [in] `hMenu`  
 메뉴에 대 한 핸들 또는 `NULL` 단추 메뉴 하지 않은 경우.  
  
 [in] `iImage`  
 단추;에 대 한 이미지의 인덱스 그렇지 않으면-1이이 단추에 아이콘 없거나 지정 된 명령에 대 한 아이콘을 사용 하 여 `uiID`합니다. 인덱스는 각각에 대해 동일한 `CMFCToolBarImages` 응용 프로그램의 개체입니다.  
  
 [in] `lpszText`  
 도구 모음 메뉴 단추의 텍스트입니다.  
  
 [in] `bUserButton`  
 `TRUE`단추는 사용자 지정 이미지를 표시 하는 경우 `FALSE` 단추에 의해 지정 된 명령에 연결 된 미리 정의 된 이미지를 표시 하는 경우 `uiID`합니다.  
  
### <a name="remarks"></a>주의  
 경우 `uiID` 유효한 명령 ID, 단추는 사용자가 해당 명령을 수행 합니다. 경우 `hMenu` 유효한 메뉴 핸들 단추 메뉴에 표시 될 경우 도구 모음 또는 하위 메뉴에 표시 될 경우 드롭다운 메뉴를 제공 합니다. 모두 `uiID` 및 `hMenu` 단추는 사용자가 클릭 될 때 명령을 수행할 부분과 아래쪽 화살표가 있는 됩니다 드롭 다운 메뉴에서 사용자가 클릭 하면 일부 분할-단추 유효 합니다. 그러나 경우 `hMenu` 유효 사용자 메뉴에 있는 단추를 삽입 하면 명령을 수행 하려면 단추를 클릭 하 여 수행할 수 없습니다.  
  
### <a name="example"></a>예제  
 개체를 생성 하는 방법은 다음 예제는 `CMFCToolBarMenuButton` 클래스입니다. 이 코드 조각은의 일부인는 [워드 패드 샘플](../../visual-cpp-samples.md)합니다.  
  
 [!code-cpp[NVC_MFC_WordPad #&9;](../../mfc/reference/codesnippet/cpp/cmfctoolbarmenubutton-class_2.cpp)]  
  
##  <a name="comparewith"></a>CMFCToolBarMenuButton::CompareWith  

  
```  
virtual BOOL CompareWith(const CMFCToolBarButton& other) const;  
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `other`  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>주의  
  
##  <a name="copyfrom"></a>CMFCToolBarMenuButton::CopyFrom  

  
```  
virtual void CopyFrom(const CMFCToolBarButton& src);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `src`  
  
### <a name="remarks"></a>주의  
  
##  <a name="createfrommenu"></a>CMFCToolBarMenuButton::CreateFromMenu  
 창 메뉴 핸들에서 도구 모음 메뉴를 초기화합니다.  
  
```  
virtual void CreateFromMenu(HMENU hMenu);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `hMenu`  
 메뉴에 대 한 핸들입니다.  
  
### <a name="remarks"></a>주의  
 도구 모음 메뉴 단추의 드롭 다운 하위 메뉴를 표시할 수 있습니다.  
  
 프레임 워크의 명령 메뉴에서 하위 메뉴에서 초기화 하려면이 메서드를 호출 합니다.  
  
##  <a name="createmenu"></a>CMFCToolBarMenuButton::CreateMenu  
 도구 모음 메뉴의 명령으로 구성 된 메뉴를 만듭니다. 메뉴에 대 한 핸들을 반환합니다.  
  
```  
virtual HMENU CreateMenu() const;  
```  
  
### <a name="return-value"></a>반환 값  
 메뉴에 대 한 경우 A 핸들 성공 합니다. `NULL`도구 모음 메뉴 단추와 연결 된 명령 목록이 비어 있습니다.  
  
### <a name="remarks"></a>주의  
 메뉴에 생성 되는 방법을 사용자 지정 하는 파생된 클래스에서이 메서드를 재정의할 수 있습니다.  
  
##  <a name="createpopupmenu"></a>CMFCToolBarMenuButton::CreatePopupMenu  
 만듭니다는 `CMFCPopupMenu` 도구 모음 메뉴를 표시 하는 개체입니다.  
  
```  
virtual CMFCPopupMenu* CreatePopupMenu();
```  
  
### <a name="return-value"></a>반환 값  
 에 대 한 포인터는 `CMFCPopupMenu` 도구 모음 메뉴 단추와 연결 된 드롭다운 메뉴를 표시 하는 개체입니다.  
  
### <a name="remarks"></a>주의  
 이 메서드는 단추와 연결 된 드롭다운 메뉴의 표시를 준비 하는 프레임 워크에서 호출 됩니다.  
  
 기본 구현에서 방금 생성 하 고 새 반환 `CMFCPopupMenu` 개체입니다. 파생된 형식을 사용 하려는 경우이 메서드를 재정의 [CMFCPopupMenu 클래스](cmfcpopupmenu-class.md) 또는 추가 초기화를 수행 합니다.  
  
##  <a name="drawdocumenticon"></a>CMFCToolBarMenuButton::DrawDocumentIcon  
 문서 아이콘이 메뉴 단추를 그립니다.  
  
```  
void DrawDocumentIcon(
    CDC* pDC,  
    const CRect& rectImage,  
    HICON hIcon);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `pDC`  
 장치 컨텍스트에 대 한 포인터입니다.  
  
 [in] `rectImage`  
 이미지 경계 사각형의 좌표입니다.  
  
 [in] `hIcon`  
 아이콘에 대 한 핸들입니다.  
  
### <a name="remarks"></a>주의  
 이 메서드는 문서 아이콘을 사용 하 고 가운데에 의해 지정 된 영역 메뉴 단추를 그립니다 `rectImage`합니다.  
  
##  <a name="enablequickcustomize"></a>CMFCToolBarMenuButton::EnableQuickCustomize  

  
```  
void EnableQuickCustomize();
```  
  
### <a name="remarks"></a>주의  
  
##  <a name="hasbutton"></a>CMFCToolBarMenuButton::HasButton  

  
```  
virtual BOOL HasButton() const;  
```  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>주의  
  
##  <a name="havehotborder"></a>CMFCToolBarMenuButton::HaveHotBorder  

  
```  
virtual BOOL HaveHotBorder() const;  
```  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>주의  
  
##  <a name="isborder"></a>CMFCToolBarMenuButton::IsBorder  

  
```  
virtual BOOL IsBorder() const;  
```  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>주의  
  
##  <a name="isclickedonmenu"></a>CMFCToolBarMenuButton::IsClickedOnMenu  

  
```  
BOOL IsClickedOnMenu() const;  
```  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>주의  
  
##  <a name="isquickmode"></a>CMFCToolBarMenuButton::IsQuickMode  

  
```  
BOOL IsQuickMode();
```  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>주의  
  
##  <a name="getcommands"></a>CMFCToolBarMenuButton::GetCommands  
 도구 모음 메뉴에 있는 명령 목록에 대 한 읽기 전용 액세스를 제공합니다.  
  
```  
const CObList& GetCommands() const;  
```  
  
### <a name="return-value"></a>반환 값  
 Const에 대 한 참조는 [CObList 클래스](../../mfc/reference/coblist-class.md) 개체의 컬렉션을 포함 하는 [CMFCToolBarButton 클래스](../../mfc/reference/cmfctoolbarbutton-class.md) 개체입니다.  
  
### <a name="remarks"></a>주의  
 도구 모음 메뉴 단추는 하위 메뉴를 표시할 수 있습니다. 생성자 또는 하위 메뉴에 있는 명령의 목록을 제공할 수 있습니다 [CMFCToolBarMenuButton::CreateFromMenu](#createfrommenu) 으로 메뉴에 대 한 핸들 ( `HMENU`). 메뉴에서 파생 된 개체의 목록으로 변환 됩니다 [CMFCToolBarButton 클래스](../../mfc/reference/cmfctoolbarbutton-class.md) 내부에 저장 하 고 `CObList` 개체입니다. 이 메서드를 호출 하 여이 목록에 액세스할 수 있습니다.  
  
##  <a name="getimagerect"></a>CMFCToolBarMenuButton::GetImageRect  
 단추 이미지에 대 한 경계 사각형을 검색 합니다.  
  
```  
void GetImageRect(CRect& rectImage);
```  
  
### <a name="parameters"></a>매개 변수  
 [out] `rectImage`  
 에 대 한 참조는 `CRect` 이미지 경계 사각형의 좌표를 받는 개체입니다.  
  
##  <a name="getpaletterows"></a>CMFCToolBarMenuButton::GetPaletteRows  
 메뉴 팔레트 모드에 있을 때 드롭 다운 메뉴에서 행의 수를 반환 합니다.  
  
```  
int GetPaletteRows() const;  
```  
  
### <a name="return-value"></a>반환 값  
 색상표에 있는 행의 수입니다.  
  
### <a name="remarks"></a>주의  
 메뉴 단추 팔레트 모드로 설정 되 면 메뉴 항목의 행 수를 제한 하 여 여러 열에 표시 됩니다. 행의 수를 가져오려면이 메서드를 호출 합니다. 사용 하도록 설정 하 또는 색상표 모드를 사용 하지 않도록 설정 하 고 사용 하 여 행의 수를 지정할 수 [CMFCToolBarMenuButton::SetMenuPaletteMode](#setmenupalettemode)합니다.  
  
##  <a name="getpopupmenu"></a>CMFCToolBarMenuButton::GetPopupMenu  
 에 대 한 포인터를 반환 된 [CMFCPopupMenu 클래스](../../mfc/reference/cmfcpopupmenu-class.md) 단추의 드롭다운 메뉴를 나타내는 개체입니다.  
  
```  
CMFCPopupMenu* GetPopupMenu() const;  
```  
  
### <a name="return-value"></a>반환 값  
 에 대 한 포인터는 [CMFCPopupMenu 클래스](../../mfc/reference/cmfcpopupmenu-class.md) 프레임 워크의 하위 메뉴 도구 모음 메뉴 단추의; 그린 때 생성 된 개체 `NULL` 경우 없는 하위 메뉴가 표시 됩니다.  
  
### <a name="remarks"></a>주의  
 드롭다운 메뉴를 표시 하는 도구 모음 메뉴 단추의 경우 단추 만듭니다는 [CMFCPopupMenu 클래스](../../mfc/reference/cmfcpopupmenu-class.md) 메뉴를 나타내는 개체를 합니다. 에 대 한 포인터를 가져오려면이 메서드를 호출 하 여 `CMFCPopupMenu` 개체입니다. 임시 되 고 사용자가 드롭다운 메뉴를 닫을 때 유효 하지 않게 하기 때문에 반환 된 포인터를 저장 하지 마십시오.  
  
##  <a name="isdroppeddown"></a>CMFCToolBarMenuButton::IsDroppedDown  
 팝업 메뉴는 현재 표시 되어 있는지 여부를 나타냅니다.  
  
```  
virtual BOOL IsDroppedDown() const;  
```  
  
### <a name="return-value"></a>반환 값  
 `TRUE`도구 모음 메뉴 단추; 고 하위 메뉴를 표시 하는 경우 그렇지 않으면 `FALSE`합니다.  
  
##  <a name="isemptymenuallowed"></a>CMFCToolBarMenuButton::IsEmptyMenuAllowed  
 빈 하위 메뉴 항목에 표시 되는지 여부를 지정 합니다.  
  
```  
virtual BOOL IsEmptyMenuAllowed() const;  
```  
  
### <a name="return-value"></a>반환 값  
 `TRUE`프레임 워크의 하위 메뉴 비어 있는 경우에 현재 선택 된 메뉴 항목에서 하위 메뉴를 엽니다 하는 경우 그렇지 않으면 `FALSE`합니다.  
  
### <a name="remarks"></a>주의  
 프레임 워크는 사용자가 현재 선택 된 메뉴 항목에서의 하위 메뉴를 열고 하려고 할 때이 메서드를 호출 합니다. 하위 메뉴에서 비어 있는 경우 및 `IsEmptyMenuAllowed` 반환 `FALSE`, 하위 메뉴 열리지 것입니다.  
  
 기본 구현은 `FALSE`를 반환합니다. 이 동작을 사용자 지정 하려면이 메서드를 재정의 합니다.  
  
##  <a name="isexclusive"></a>CMFCToolBarMenuButton::IsExclusive  
 단추 단독 모드 인지 여부를 나타냅니다.  
  
```  
virtual BOOL IsExclusive() const;  
```  
  
### <a name="return-value"></a>반환 값  
 `TRUE`단추 단독 모드에서 작동 하는 경우 그렇지 않으면 `FALSE`합니다.  
  
### <a name="remarks"></a>주의  
 사용자가 다음 다른 도구 모음이 나 메뉴 단추 위로 마우스 포인터를 이동를 단추에 대 한 팝업 메뉴를 열고, 팝업 메뉴 단추 배타 모드에 있지 않으면을 닫습니다.  
  
 기본 구현에서는 항상 반환 `FALSE`합니다. 단독 모드를 설정 하려는 경우에 파생된 클래스에서이 메서드를 재정의 합니다.  
  
##  <a name="ismenupalettemode"></a>CMFCToolBarMenuButton::IsMenuPaletteMode  
 드롭다운 메뉴 팔레트 모드 인지 여부를 결정 합니다.  
  
```  
BOOL IsMenuPaletteMode() const;  
```  
  
### <a name="return-value"></a>반환 값  
 `TRUE`그렇지 않으면 팔레트 모드가 활성화 된 경우 `FALSE`합니다.  
  
### <a name="remarks"></a>주의  
 메뉴 단추 팔레트 모드로 설정 되 면 메뉴 항목의 행 수를 제한 하 여 여러 열에 나타납니다. 행의 수를 가져오려면이 메서드를 호출 합니다. 호출 하 여 색상표 모드를 사용 하지 않도록 설정 하거나 설정할 수 있습니다 [CMFCToolBarMenuButton::SetMenuPaletteMode](#setmenupalettemode)합니다.  
  
##  <a name="istearoffmenu"></a>CMFCToolBarMenuButton::IsTearOffMenu  
 드롭다운 메뉴에 분리 표시줄이 있는지 여부를 나타냅니다.  
  
```  
virtual BOOL IsTearOffMenu() const;  
```  
  
### <a name="return-value"></a>반환 값  
 `TRUE`도구 모음 메뉴 단추에 분리 표시줄이; 있으면 그렇지 않으면 `FALSE`합니다.  
  
### <a name="remarks"></a>주의  
 분리 기능을 사용 하는 분리 설정 ID, 막대 호출 [CMFCToolBarMenuButton::SetTearOff](#settearoff)합니다.  
  
##  <a name="m_balwayscallownerdraw"></a>CMFCToolBarMenuButton::m_bAlwaysCallOwnerDraw  
 프레임 워크를 항상 호출 여부를 지정 [CFrameWndEx::OnDrawMenuImage](../../mfc/reference/cframewndex-class.md#ondrawmenuimage) 단추를 그릴 때.  
  
```  
static BOOL m_bAlwaysCallOwnerDraw;  
```  
  
### <a name="remarks"></a>주의  
 이 멤버 변수를로 설정 되 면 `TRUE`, 단추를 항상 호출 [CFrameWndEx::OnDrawMenuImage](../../mfc/reference/cframewndex-class.md#ondrawmenuimage) 메서드를 단추에 이미지를 표시 합니다. 때 `m_bAlwaysCallOwnerDraw` 는 `FALSE`를 단추 자체 이미지는 미리 정의 하는 경우 이미지를 그립니다. 그렇지 않으면, 호출 `OnDrawMenuImage`합니다.  
  
##  <a name="onaftercreatepopupmenu"></a>CMFCToolBarMenuButton::OnAfterCreatePopupMenu  

  
```  
virtual void OnAfterCreatePopupMenu();
```  
  
### <a name="remarks"></a>주의  
  
##  <a name="onbeforedrag"></a>CMFCToolBarMenuButton::OnBeforeDrag  

  
```  
virtual BOOL OnBeforeDrag() const;  
```  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>주의  
  
##  <a name="oncalculatesize"></a>CMFCToolBarMenuButton::OnCalculateSize  

  
```  
virtual SIZE OnCalculateSize(
    CDC* pDC,  
    const CSize& sizeDefault,  
    BOOL bHorz);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `pDC`  
 [in] `sizeDefault`  
 [in] `bHorz`  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>주의  
  
##  <a name="oncancelmode"></a>CMFCToolBarMenuButton::OnCancelMode  

  
```  
virtual void OnCancelMode();
```  
  
### <a name="remarks"></a>주의  
  
##  <a name="onchangeparentwnd"></a>CMFCToolBarMenuButton::OnChangeParentWnd  

  
```  
virtual void OnChangeParentWnd(CWnd* pWndParent);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `pWndParent`  
  
### <a name="remarks"></a>주의  
  
##  <a name="onclick"></a>CMFCToolBarMenuButton::OnClick  

  
```  
virtual BOOL OnClick(
    CWnd* pWnd,  
    BOOL bDelay = TRUE);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `pWnd`  
 [in] `bDelay`  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>주의  
  
##  <a name="onclickmenuitem"></a>CMFCToolBarMenuButton::OnClickMenuItem  
 드롭 다운 메뉴에서 항목을 선택할 때 프레임 워크에서 호출 합니다.  
  
```  
virtual BOOL OnClickMenuItem();
```  
  
### <a name="return-value"></a>반환 값  
 `FALSE`프레임 워크의 기본 메뉴 항목 처리를 계속 해야 하는 경우 그렇지 않으면 `TRUE`합니다. 기본 구현에서는 항상 반환 `FALSE`합니다.  
  
### <a name="remarks"></a>주의  
 사용자가 메뉴 항목을 클릭할 때 프레임 워크는 해당 항목과 연결 되는 명령을 실행 합니다.  
  
 메뉴 항목 처리를 사용자 지정 하려면 재정의 `OnClickMenuItem` 에서 파생 된 클래스에서 `CMFCToolBarMenuButton` 클래스입니다. 재정의 해야 [CFrameWndEx::OnShowPopupMenu](../../mfc/reference/cframewndex-class.md#onshowpopupmenu) 파생된 클래스의 인스턴스를 사용 하 여 특수 처리를 필요로 하는 메뉴 단추를 바꿉니다.  
  
##  <a name="oncontexthelp"></a>CMFCToolBarMenuButton::OnContextHelp  

  
```  
virtual BOOL OnContextHelp(CWnd* pWnd);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `pWnd`  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>주의  
  
##  <a name="ondraw"></a>CMFCToolBarMenuButton::OnDraw  

  
```  
virtual void OnDraw(
    CDC* pDC,  
    const CRect& rect,  
    CMFCToolBarImages* pImages,  
    BOOL bHorz = TRUE,  
    BOOL bCustomizeMode = FALSE,  
    BOOL bHighlight = FALSE,  
    BOOL bDrawBorder = TRUE,  
    BOOL bGrayDisabledButtons = TRUE);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `pDC`  
 [in] `rect`  
 [in] `pImages`  
 [in] `bHorz`  
 [in] `bCustomizeMode`  
 [in] `bHighlight`  
 [in] `bDrawBorder`  
 [in] `bGrayDisabledButtons`  
  
### <a name="remarks"></a>주의  
  
##  <a name="ondrawoncustomizelist"></a>CMFCToolBarMenuButton::OnDrawOnCustomizeList  

  
```  
virtual int OnDrawOnCustomizeList(
    CDC* pDC,  
    const CRect& rect,  
    BOOL bSelected);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `pDC`  
 [in] `rect`  
 [in] `bSelected`  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>주의  
  
##  <a name="openpopupmenu"></a>CMFCToolBarMenuButton::OpenPopupMenu  
 사용자가 도구 모음 메뉴 단추의 드롭다운 메뉴를 열 때 프레임 워크에서 호출 합니다.  
  
```  
virtual BOOL OpenPopupMenu(CWnd* pWnd=NULL);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `pWnd`  
 드롭다운 메뉴 명령을 수신 하는 기간을 지정 합니다. 수 `NULL` 도구 모음 메뉴 단추 부모 창에 경우에 있습니다.  
  
### <a name="return-value"></a>반환 값  
 `TRUE`경우는 [CMFCPopupMenu 클래스](../../mfc/reference/cmfcpopupmenu-class.md) 개체 생성 되어 성공적으로 고, 그렇지 않으면 열 `FALSE`합니다.  
  
### <a name="remarks"></a>주의  
 이 함수는 사용자가 도구 모음 메뉴 단추에서 드롭다운 메뉴를 열 때 프레임 워크에 의해 호출 됩니다.  
  
##  <a name="resetimagetodefault"></a>CMFCToolBarMenuButton::ResetImageToDefault  

  
```  
virtual void ResetImageToDefault();
```  
  
### <a name="remarks"></a>주의  
  
##  <a name="savebarstate"></a>CMFCToolBarMenuButton::SaveBarState  

  
```  
virtual void SaveBarState();
```  
  
### <a name="remarks"></a>주의  
 프레임 워크는 끌어서 놓기 작업의 결과로 도구 모음 단추를 만들 때이 메서드를 호출 합니다. 이 메서드는 [CMFCPopupMenu::SaveState](../../mfc/reference/cmfcpopupmenu-class.md#savestate) 메서드를 다시 해당 메뉴 팝업 메뉴의 부모 단추가 최상위 팝업 메뉴의 합니다.  
  
##  <a name="serialize"></a>CMFCToolBarMenuButton::Serialize  

  
```  
virtual void Serialize(CArchive& ar);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `ar`  
  
### <a name="remarks"></a>주의  
  
##  <a name="setaccdata"></a>CMFCToolBarMenuButton::SetACCData  
 리본 요소에 대한 내게 필요한 옵션 데이터를 설정합니다.  
  
```  
virtual BOOL SetACCData(
    CWnd* pParent,  
    CAccessibilityData& data);
```  
  
### <a name="parameters"></a>매개 변수  
 `pParent`  
 리본 요소에 대한 부모 창입니다.  
  
 `data`  
 리본 요소에 대한 내게 필요한 옵션 데이터입니다.  
  
### <a name="return-value"></a>반환 값  
 항상 `TRUE`를 반환합니다.  
  
### <a name="remarks"></a>주의  
 기본적으로 이 메서드는 리본 요소에 대한 내게 필요한 옵션 데이터를 설정하고 항상 `TRUE`를 반환합니다. 내게 필요한 옵션 데이터를 설정하고 성공 또는 실패를 나타내는 값을 반환하려면 이 메서드를 재정의합니다.  
  
##  <a name="setmenuonly"></a>CMFCToolBarMenuButton::SetMenuOnly  
 올바른 명령 ID와 하위 메뉴에 있을 때 단추 메뉴 단추 또는 분할 단추도 그릴지 여부를 지정 합니다.  
  
```  
void SetMenuOnly(BOOL bMenuOnly);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `bMenuOnly`  
 `TRUE`유효한 명령 ID와 하위 메뉴에 있을 때이 단추를 메뉴 단추로 표시 하 `FALSE` 유효한 명령 ID와 하위 메뉴에 있을 때 분할 단추와이 단추를 표시 합니다.  
  
### <a name="remarks"></a>주의  
 일반적으로 도구 모음 메뉴 단추에는 하위 메뉴 및 명령 ID를 모두 있는 경우 메뉴는 아래쪽 화살표 단추에는 기본 단추 및 연결 된 분할 단추 것 같습니다. 이 메서드를 호출 하 고 `bMenuOnly` 는 `TRUE`, 단추 대신 단추에서 아래쪽 화살표를 사용 하는 단일 메뉴 단추를 표시 합니다. 사용자가 두 모드에 있는 화살표를 클릭 하면 하위 메뉴에서 열리고 클릭할 모드나 프레임 워크 단추의 비 화살표 부분 명령을 실행 합니다.  
  
##  <a name="setmenupalettemode"></a>CMFCToolBarMenuButton::SetMenuPaletteMode  
 드롭다운 메뉴 팔레트 모드 인지 여부를 지정 합니다.  
  
```  
void SetMenuPaletteMode(
    BOOL bMenuPaletteMode=TRUE,  
    int nPaletteRows=1);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `bMenuPaletteMode`  
 드롭다운 메뉴 팔레트 모드 인지 여부를 지정 합니다.  
  
 [in] `nPaletteRows`  
 색상표에 있는 행의 수입니다.  
  
### <a name="remarks"></a>주의  
 팔레트 모드에서 모든 메뉴 항목은 여러 열 팔레트도 표시 됩니다. 사용 하 여 행의 수를 지정 `nPaletteRows`합니다.  
  
##  <a name="setmessagewnd"></a>CMFCToolBarMenuButton::SetMessageWnd  

  
```  
void SetMessageWnd(CWnd* pWndMessage);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `pWndMessage`  
  
### <a name="remarks"></a>주의  
  
##  <a name="setradio"></a>CMFCToolBarMenuButton::SetRadio  
 선택 시 라디오 단추 스타일 아이콘을 표시 하려면 도구 모음 메뉴 단추를 설정 합니다.  
  
```  
virtual void SetRadio();
```  
  
### <a name="remarks"></a>주의  
 호출 하 고 메뉴 단추를 선택 하는 동안을 그릴 때 [CMFCVisualManager::OnDrawMenuCheck](../../mfc/reference/cmfcvisualmanager-class.md#ondrawmenucheck) 확인 표시 아이콘을 그리는 데 있습니다. 기본적으로 `OnDrawMenuCheck` 현재 비주얼 관리자 확인란을 그립니다 요청 확인 표시 메뉴 단추 스타일 지정 합니다. 이 메서드를 호출 하면 현재 비주얼 관리자를 대신 라디오 단추 스타일 확인 표시 메뉴 단추를 그립니다. 이 변경 내용을 취소할 수 없습니다.  
  
 이 메서드를 호출 하는 경우 메뉴 단추 표시 되 고 새로 고쳐집니다.  
  
##  <a name="settearoff"></a>CMFCToolBarMenuButton::SetTearOff  
 드롭다운 메뉴에 대 한 분리 표시줄의 ID를 지정 합니다.  
  
```  
virtual void SetTearOff(UINT uiBarID);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `uiBarID`  
 새 분리 지정 막대 id입니다.  
  
### <a name="remarks"></a>주의  
 메뉴 모음에서 메뉴 단추를 끌 때 만들어지는 분리 표시줄에 대 한 ID를 지정 하려면이 메서드를 호출 합니다. 하는 경우는 `uiBarID` 매개 변수가 0 이면 사용자 메뉴 단추 떼어낼 수 없습니다.  
  
 호출 [CWinAppEx::EnableTearOffMenus](../../mfc/reference/cwinappex-class.md#enabletearoffmenus) 응용 프로그램에서 분리 메뉴 기능을 활성화 합니다.  
  
## <a name="see-also"></a>참고 항목  
 [계층 구조 차트](../../mfc/hierarchy-chart.md)   
 [클래스](../../mfc/reference/mfc-classes.md)   
 [CMFCToolBarButton 클래스](../../mfc/reference/cmfctoolbarbutton-class.md)   
 [CMFCToolBar 클래스](../../mfc/reference/cmfctoolbar-class.md)   
 [CMFCPopupMenu 클래스](../../mfc/reference/cmfcpopupmenu-class.md)