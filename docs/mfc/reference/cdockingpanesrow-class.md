---
title: "CDockingPanesRow 클래스 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- CDockingPanesRow
- AFXDOCKINGPANESROW/CDockingPanesRow
- AFXDOCKINGPANESROW/CDockingPanesRow::AddPane
- AFXDOCKINGPANESROW/CDockingPanesRow::AddPaneFromRow
- AFXDOCKINGPANESROW/CDockingPanesRow::ArrangePanes
- AFXDOCKINGPANESROW/CDockingPanesRow::CalcFixedLayout
- AFXDOCKINGPANESROW/CDockingPanesRow::Create
- AFXDOCKINGPANESROW/CDockingPanesRow::ExpandStretchedPanes
- AFXDOCKINGPANESROW/CDockingPanesRow::ExpandStretchedPanesRect
- AFXDOCKINGPANESROW/CDockingPanesRow::FixupVirtualRects
- AFXDOCKINGPANESROW/CDockingPanesRow::GetAvailableLength
- AFXDOCKINGPANESROW/CDockingPanesRow::GetAvailableSpace
- AFXDOCKINGPANESROW/CDockingPanesRow::GetClientRect
- AFXDOCKINGPANESROW/CDockingPanesRow::GetDockSite
- AFXDOCKINGPANESROW/CDockingPanesRow::GetExtraSpace
- AFXDOCKINGPANESROW/CDockingPanesRow::GetGroupFromPane
- AFXDOCKINGPANESROW/CDockingPanesRow::GetID
- AFXDOCKINGPANESROW/CDockingPanesRow::GetMaxPaneSize
- AFXDOCKINGPANESROW/CDockingPanesRow::GetPaneCount
- AFXDOCKINGPANESROW/CDockingPanesRow::GetPaneList
- AFXDOCKINGPANESROW/CDockingPanesRow::GetRowAlignment
- AFXDOCKINGPANESROW/CDockingPanesRow::GetRowHeight
- AFXDOCKINGPANESROW/CDockingPanesRow::GetRowOffset
- AFXDOCKINGPANESROW/CDockingPanesRow::GetVisibleCount
- AFXDOCKINGPANESROW/CDockingPanesRow::GetWindowRect
- AFXDOCKINGPANESROW/CDockingPanesRow::HasPane
- AFXDOCKINGPANESROW/CDockingPanesRow::IsEmpty
- AFXDOCKINGPANESROW/CDockingPanesRow::IsExclusiveRow
- AFXDOCKINGPANESROW/CDockingPanesRow::IsHorizontal
- AFXDOCKINGPANESROW/CDockingPanesRow::IsVisible
- AFXDOCKINGPANESROW/CDockingPanesRow::Move
- AFXDOCKINGPANESROW/CDockingPanesRow::MovePane
- AFXDOCKINGPANESROW/CDockingPanesRow::OnResizePane
- AFXDOCKINGPANESROW/CDockingPanesRow::RedrawAll
- AFXDOCKINGPANESROW/CDockingPanesRow::RemovePane
- AFXDOCKINGPANESROW/CDockingPanesRow::ReplacePane
- AFXDOCKINGPANESROW/CDockingPanesRow::RepositionPanes
- AFXDOCKINGPANESROW/CDockingPanesRow::Resize
- AFXDOCKINGPANESROW/CDockingPanesRow::ResizeByPaneDivider
- AFXDOCKINGPANESROW/CDockingPanesRow::ScreenToClient
- AFXDOCKINGPANESROW/CDockingPanesRow::SetExtra
- AFXDOCKINGPANESROW/CDockingPanesRow::ShowDockSiteRow
- AFXDOCKINGPANESROW/CDockingPanesRow::ShowPane
- AFXDOCKINGPANESROW/CDockingPanesRow::UpdateVisibleState
dev_langs:
- C++
helpviewer_keywords:
- CDockingPanesRow class
ms.assetid: e7a17832-0ebb-4bce-b799-cec9b60f76fe
caps.latest.revision: 25
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
ms.openlocfilehash: c9f9b975f5ee60c418c1a4c223183a8cfed31926
ms.contentlocale: ko-kr
ms.lasthandoff: 02/24/2017

---
# <a name="cdockingpanesrow-class"></a>CDockingPanesRow 클래스
도크 사이트의 동일한 수평 또는 수직 행(열)에 위치한 창 목록을 관리합니다.  

 [!INCLUDE[cpp_fp_under_construction](../../mfc/reference/includes/cpp_fp_under_construction_md.md)]  
  
## <a name="syntax"></a>구문  
  
```  
class CDockingPanesRow : public CObject  
```  
  
## <a name="members"></a>멤버  
  
### <a name="public-constructors"></a>Public 생성자  
  
|이름|설명|  
|----------|-----------------|  
|`CDockingPanesRow::CDockingPanesRow`|기본 생성자입니다.|  
  
### <a name="public-methods"></a>Public 메서드  
  
|이름|설명|  
|----------|-----------------|  
|[CDockingPanesRow::AddPane](#addpane)||  
|[CDockingPanesRow::AddPaneFromRow](#addpanefromrow)||  
|[CDockingPanesRow::ArrangePanes](#arrangepanes)|지정된 여백 및 간격 매개 변수에 따라 창을 일렬로 정렬합니다.|  
|[CDockingPanesRow::CalcFixedLayout](#calcfixedlayout)||  
|[CDockingPanesRow::Create](#create)||  
|[CDockingPanesRow::ExpandStretchedPanes](#expandstretchedpanes)||  
|[CDockingPanesRow::ExpandStretchedPanesRect](#expandstretchedpanesrect)||  
|[CDockingPanesRow::FixupVirtualRects](#fixupvirtualrects)||  
|[CDockingPanesRow::GetAvailableLength](#getavailablelength)||  
|[CDockingPanesRow::GetAvailableSpace](#getavailablespace)||  
|[CDockingPanesRow::GetClientRect](#getclientrect)||  
|[CDockingPanesRow::GetDockSite](#getdocksite)||  
|[CDockingPanesRow::GetExtraSpace](#getextraspace)||  
|[CDockingPanesRow::GetGroupFromPane](#getgroupfrompane)||  
|[CDockingPanesRow::GetID](#getid)||  
|[CDockingPanesRow::GetMaxPaneSize](#getmaxpanesize)||  
|[CDockingPanesRow::GetPaneCount](#getpanecount)||  
|[CDockingPanesRow::GetPaneList](#getpanelist)||  
|[CDockingPanesRow::GetRowAlignment](#getrowalignment)||  
|[CDockingPanesRow::GetRowHeight](#getrowheight)||  
|[CDockingPanesRow::GetRowOffset](#getrowoffset)||  
|[CDockingPanesRow::GetVisibleCount](#getvisiblecount)||  
|[CDockingPanesRow::GetWindowRect](#getwindowrect)||  
|[CDockingPanesRow::HasPane](#haspane)||  
|[CDockingPanesRow::IsEmpty](#isempty)||  
|[CDockingPanesRow::IsExclusiveRow](#isexclusiverow)||  
|[CDockingPanesRow::IsHorizontal](#ishorizontal)||  
|[CDockingPanesRow::IsVisible](#isvisible)||  
|[CDockingPanesRow::Move](#move)||  
|[CDockingPanesRow::MovePane](#movepane)||  
|[CDockingPanesRow::OnResizePane](#onresizepane)||  
|[CDockingPanesRow::RedrawAll](#redrawall)||  
|[CDockingPanesRow::RemovePane](#removepane)||  
|[CDockingPanesRow::ReplacePane](#replacepane)||  
|[CDockingPanesRow::RepositionPanes](#repositionpanes)||  
|[CDockingPanesRow::Resize](#resize)||  
|[CDockingPanesRow::ResizeByPaneDivider](#resizebypanedivider)||  
|[CDockingPanesRow::ScreenToClient](#screentoclient)||  
|[CDockingPanesRow::SetExtra](#setextra)||  
|[CDockingPanesRow::ShowDockSiteRow](#showdocksiterow)||  
|[CDockingPanesRow::ShowPane](#showpane)||  
|[CDockingPanesRow::UpdateVisibleState](#updatevisiblestate)||  
  
## <a name="remarks"></a>주의  
 `CDockingPanesRow` 개체는 도킹 사이트 개체에 의해 내부적으로 만들어집니다.  
  
## <a name="example"></a>예제  
 다음 예제에서는 `CMFCAutoHideBar` 개체에서 `CDockingPanesRow` 개체를 가져오는 방법을 보여 줍니다.  
  
 [!code-cpp[NVC_MFC_RibbonApp #&26;](../../mfc/reference/codesnippet/cpp/cdockingpanesrow-class_1.cpp)]  
  
## <a name="inheritance-hierarchy"></a>상속 계층  
 [CObject](../../mfc/reference/cobject-class.md)  
  
 [CDockingPanesRow](../../mfc/reference/cdockingpanesrow-class.md)  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** afxDockingPanesRow.h  
  
##  <a name="addpane"></a>CDockingPanesRow::AddPane  

  
```  
virtual void AddPane(
    CPane* pControlBar,  
    AFX_DOCK_METHOD dockMethod,  
    LPCRECT lpRect = NULL,  
    BOOL bAddLast = FALSE);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `pControlBar`  
 [in] `dockMethod`  
 [in] `lpRect`  
 [in] `bAddLast`  
  
### <a name="remarks"></a>주의  
  
##  <a name="addpanefromrow"></a>CDockingPanesRow::AddPaneFromRow  

  
```  
virtual void AddPaneFromRow(
    CPane* pControlBar,  
    AFX_DOCK_METHOD dockMethod);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `pControlBar`  
 [in] `dockMethod`  
  
### <a name="remarks"></a>주의  
  
##  <a name="arrangepanes"></a>CDockingPanesRow::ArrangePanes  
 지정 된 여백에 따라 행의 창을 도킹 및 매개 변수를 간격을 정렬 합니다.  
  
```  
virtual void ArrangePanes(
    int nMargin,  
    int nSpacing);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `nMargin`  
 첫 번째 창에서 행의 왼쪽 위 모퉁이 픽셀 단위로 오프셋을 지정합니다.  
  
 [in] `nSpacing`  
 픽셀 단위로 창 사이의 간격을 지정합니다.  
  
### <a name="remarks"></a>주의  
 창 도킹 됩니다 있는 행의 정렬 하려면이 메서드를 호출 합니다. 이 메서드를 호출한 후 `CDockingPanesRow::FixupVirtualRects(FALSE, NULL)`합니다.  
  
##  <a name="calcfixedlayout"></a>CDockingPanesRow::CalcFixedLayout  

  
```  
virtual CSize CalcFixedLayout(
    BOOL bStretch,  
    BOOL bHorz);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `bStretch`  
 [in] `bHorz`  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>주의  
  
##  <a name="cdockingpanesrow"></a>CDockingPanesRow::CDockingPanesRow  

  
```  
CDockingPanesRow(
    CDockSite* pParentDockBar,  
    int nOffset,  
    int nHeight);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `pParentDockBar`  
 [in] `nOffset`  
 [in] `nHeight`  
  
### <a name="remarks"></a>주의  
  
##  <a name="create"></a>CDockingPanesRow::Create  

  
```  
virtual BOOL Create();
```  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>주의  
  
##  <a name="expandstretchedpanes"></a>CDockingPanesRow::ExpandStretchedPanes  

  
```  
void ExpandStretchedPanes();
```  
  
### <a name="remarks"></a>주의  
  
##  <a name="expandstretchedpanesrect"></a>CDockingPanesRow::ExpandStretchedPanesRect  

  
```  
void ExpandStretchedPanesRect();
```  
  
### <a name="remarks"></a>주의  
  
##  <a name="fixupvirtualrects"></a>CDockingPanesRow::FixupVirtualRects  

  
```  
void FixupVirtualRects(
    bool bMoveBackToVirtualRect,  
    CPane* pBarToExclude = NULL);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `bMoveBackToVirtualRect`  
 [in] `pBarToExclude`  
  
### <a name="remarks"></a>주의  
  
##  <a name="getavailablelength"></a>CDockingPanesRow::GetAvailableLength  

  
```  
virtual int GetAvailableLength(BOOL bUseVirtualRect = FALSE) const;  
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `bUseVirtualRect`  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>주의  
  
##  <a name="getavailablespace"></a>CDockingPanesRow::GetAvailableSpace  

  
```  
virtual void GetAvailableSpace(CRect& rect);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `rect`  
  
### <a name="remarks"></a>주의  
  
##  <a name="getclientrect"></a>CDockingPanesRow::GetClientRect  

  
```  
void GetClientRect(CRect& rect) const;  
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `rect`  
  
### <a name="remarks"></a>주의  
  
##  <a name="getdocksite"></a>CDockingPanesRow::GetDockSite  

  
```  
CDockSite* GetDockSite() const;  
```  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>주의  
  
##  <a name="getextraspace"></a>CDockingPanesRow::GetExtraSpace  

  
```  
int GetExtraSpace() const;  
```  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>주의  
  
##  <a name="getgroupfrompane"></a>CDockingPanesRow::GetGroupFromPane  

  
```  
void GetGroupFromPane(
    CPane* pBar,  
    CObList& lst);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `pBar`  
 [in] `lst`  
  
### <a name="remarks"></a>주의  
  
##  <a name="getid"></a>CDockingPanesRow::GetID  

  
```  
int GetID() const;  
```  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>주의  
  
##  <a name="getmaxpanesize"></a>CDockingPanesRow::GetMaxPaneSize  

  
```  
int GetMaxPaneSize(BOOL bSkipHiddenBars = TRUE) const;  
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `bSkipHiddenBars`  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>주의  
  
##  <a name="getpanecount"></a>CDockingPanesRow::GetPaneCount  

  
```  
int GetPaneCount() const;  
```  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>주의  
  
##  <a name="getpanelist"></a>CDockingPanesRow::GetPaneList  

  
```  
const CObList& GetPaneList() const;  
```  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>주의  
  
##  <a name="getrowalignment"></a>CDockingPanesRow::GetRowAlignment  

  
```  
DWORD GetRowAlignment() const;  
```  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>주의  
  
##  <a name="getrowheight"></a>CDockingPanesRow::GetRowHeight  

  
```  
int GetRowHeight() const;  
```  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>주의  
  
##  <a name="getrowoffset"></a>CDockingPanesRow::GetRowOffset  

  
```  
int GetRowOffset() const;  
```  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>주의  
  
##  <a name="getvisiblecount"></a>CDockingPanesRow::GetVisibleCount  

  
```  
virtual int GetVisibleCount();
```  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>주의  
  
##  <a name="getwindowrect"></a>CDockingPanesRow::GetWindowRect  

  
```  
void GetWindowRect(CRect& rect) const;  
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `rect`  
  
### <a name="remarks"></a>주의  
  
##  <a name="haspane"></a>CDockingPanesRow::HasPane  

  
```  
BOOL HasPane(CBasePane* pControlBar);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `pControlBar`  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>주의  
  
##  <a name="isempty"></a>CDockingPanesRow::IsEmpty  

  
```  
virtual BOOL IsEmpty() const;  
```  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>주의  
  
##  <a name="isexclusiverow"></a>CDockingPanesRow::IsExclusiveRow  

  
```  
virtual BOOL IsExclusiveRow() const;  
```  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>주의  
  
##  <a name="ishorizontal"></a>CDockingPanesRow::IsHorizontal  

  
```  
bool IsHorizontal() const;  
```  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>주의  
  
##  <a name="isvisible"></a>CDockingPanesRow::IsVisible  

  
```  
virtual BOOL IsVisible() const;  
```  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>주의  
  
##  <a name="move"></a>CDockingPanesRow::Move  

  
```  
virtual void Move(int nOffset);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `nOffset`  
  
### <a name="remarks"></a>주의  
  
##  <a name="movepane"></a>CDockingPanesRow::MovePane  

  
```  
void MovePane(
    CPane* pControlBar,  
    CPoint ptOffset,  
    BOOL bSwapControlBars,  
    HDWP& hdwp);

 
void MovePane(
    CPane* pControlBar,  
    CRect rectTarget,  
    HDWP& hdwp);

 
void MovePane(
    CPane* pControlBar,  
    int nOffset,  
    bool bForward,  
    HDWP& hdwp);

 
void MovePane(
    CPane* pControlBar,  
    int nAbsolutOffset,  
    HDWP& hdwp);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `pControlBar`  
 [in] `ptOffset`  
 [in] `bSwapControlBars`  
 [in] `hdwp`  
 [in] `rectTarget`  
 [in] `nOffset`  
 [in] `bForward`  
 [in] `nAbsolutOffset`  
  
### <a name="remarks"></a>주의  
  
##  <a name="onresizepane"></a>CDockingPanesRow::OnResizePane  

  
```  
virtual void OnResizePane(CBasePane* pControlBar);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `pControlBar`  
  
### <a name="remarks"></a>주의  
  
##  <a name="redrawall"></a>CDockingPanesRow::RedrawAll  

  
```  
void RedrawAll();
```  
  
### <a name="remarks"></a>주의  
  
##  <a name="removepane"></a>CDockingPanesRow::RemovePane  

  
```  
virtual void RemovePane(CPane* pControlBar);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `pControlBar`  
  
### <a name="remarks"></a>주의  
  
##  <a name="replacepane"></a>CDockingPanesRow::ReplacePane  

  
```  
virtual BOOL ReplacePane(
    CPane* pBarOld,  
    CPane* pBarNew);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `pBarOld`  
 [in] `pBarNew`  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>주의  
  
##  <a name="repositionpanes"></a>CDockingPanesRow::RepositionPanes  

  
```  
virtual void RepositionPanes(
    CRect& rectNewParentBarArea,  
    UINT nSide = (UINT)-1,  
    BOOL bExpand = FALSE,  
    int nOffset = 0);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `rectNewParentBarArea`  
 [in] `nSide`  
 [in] `bExpand`  
 [in] `nOffset`  
  
### <a name="remarks"></a>주의  
  
##  <a name="resize"></a>CDockingPanesRow::Resize  

  
```  
virtual int Resize(int nOffset);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `nOffset`  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>주의  
  
##  <a name="resizebypanedivider"></a>CDockingPanesRow::ResizeByPaneDivider  

  
```  
virtual int ResizeByPaneDivider(int);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `int`  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>주의  
  
##  <a name="screentoclient"></a>CDockingPanesRow::ScreenToClient  

  
```  
void ScreenToClient(CRect& rect) const;  
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `rect`  
  
### <a name="remarks"></a>주의  
  
##  <a name="setextra"></a>CDockingPanesRow::SetExtra  

  
```  
void SetExtra(
    int nExtraSpace,  
    AFX_ROW_ALIGNMENT rowExtraAlign);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `nExtraSpace`  
 [in] `rowExtraAlign`  
  
### <a name="remarks"></a>주의  
  
##  <a name="showdocksiterow"></a>CDockingPanesRow::ShowDockSiteRow  

  
```  
virtual void ShowDockSiteRow(
    BOOL bShow,  
    BOOL bDelay);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `bShow`  
 [in] `bDelay`  
  
### <a name="remarks"></a>주의  
  
##  <a name="showpane"></a>CDockingPanesRow::ShowPane  

  
```  
virtual BOOL ShowPane(
    CPane* pControlBar,  
    BOOL bShow,  
    BOOL bDelay = FALSE);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `pControlBar`  
 [in] `bShow`  
 [in] `bDelay`  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>주의  
  
##  <a name="updatevisiblestate"></a>CDockingPanesRow::UpdateVisibleState  

  
```  
virtual void UpdateVisibleState(BOOL bDelay);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `bDelay`  
  
### <a name="remarks"></a>주의  
  
## <a name="see-also"></a>참고 항목  
 [계층 구조 차트](../../mfc/hierarchy-chart.md)   
 [클래스](../../mfc/reference/mfc-classes.md)   
 [CObject 클래스](../../mfc/reference/cobject-class.md)   
 [CDockSite 클래스](../../mfc/reference/cdocksite-class.md)   
 [CPane 클래스](../../mfc/reference/cpane-class.md)
