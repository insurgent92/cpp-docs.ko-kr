---
title: "CPagerCtrl 클래스 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- CPagerCtrl
- AFXCMN/CPagerCtrl
- AFXCMN/CPagerCtrl::CPagerCtrl
- AFXCMN/CPagerCtrl::Create
- AFXCMN/CPagerCtrl::CreateEx
- AFXCMN/CPagerCtrl::ForwardMouse
- AFXCMN/CPagerCtrl::GetBkColor
- AFXCMN/CPagerCtrl::GetBorder
- AFXCMN/CPagerCtrl::GetButtonSize
- AFXCMN/CPagerCtrl::GetButtonState
- AFXCMN/CPagerCtrl::GetDropTarget
- AFXCMN/CPagerCtrl::GetScrollPos
- AFXCMN/CPagerCtrl::IsButtonDepressed
- AFXCMN/CPagerCtrl::IsButtonGrayed
- AFXCMN/CPagerCtrl::IsButtonHot
- AFXCMN/CPagerCtrl::IsButtonInvisible
- AFXCMN/CPagerCtrl::IsButtonNormal
- AFXCMN/CPagerCtrl::RecalcSize
- AFXCMN/CPagerCtrl::SetBkColor
- AFXCMN/CPagerCtrl::SetBorder
- AFXCMN/CPagerCtrl::SetButtonSize
- AFXCMN/CPagerCtrl::SetChild
- AFXCMN/CPagerCtrl::SetScrollPos
dev_langs:
- C++
helpviewer_keywords:
- CPagerCtrl class
ms.assetid: 65ac58dd-4f5e-4b7e-b15c-e0d435a7e884
caps.latest.revision: 26
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
ms.openlocfilehash: 8b8bf05873239f274a9b1285797c01123fe071f7
ms.contentlocale: ko-kr
ms.lasthandoff: 02/24/2017

---
# <a name="cpagerctrl-class"></a>CPagerCtrl 클래스
`CPagerCtrl` 클래스는 윈도우에 맞지 않는 포함된 창을 보기로 스크롤할 수 있는 Windows 페이저 컨트롤을 래핑합니다.  
  
## <a name="syntax"></a>구문  
  
```  
class CPagerCtrl : public CWnd  
```  
  
## <a name="members"></a>멤버  
  
### <a name="public-constructors"></a>Public 생성자  
  
|이름|설명|  
|----------|-----------------|  
|[CPagerCtrl::CPagerCtrl](#cpagerctrl)|`CPagerCtrl` 개체를 생성합니다.|  
  
### <a name="public-methods"></a>Public 메서드  
  
|이름|설명|  
|----------|-----------------|  
|[CPagerCtrl::Create](#create)|지정 된 스타일으로 페이저 컨트롤을 만들고 현재 연결 `CPagerCtrl` 개체입니다.|  
|[CPagerCtrl::CreateEx](#createex)|확장된 스타일을 지정된 하 여 페이저 컨트롤을 만들고 현재 연결 `CPagerCtrl` 개체입니다.|  
|[CPagerCtrl::ForwardMouse](#forwardmouse)|설정 하거나 해제 전달 [WM_MOUSEMOVE](http://msdn.microsoft.com/library/windows/desktop/ms645616) 메시지는 현재 페이저 컨트롤에 포함 된 창입니다.|  
|[CPagerCtrl::GetBkColor](#getbkcolor)|현재 페이저 컨트롤의 배경색을 검색합니다.|  
|[CPagerCtrl::GetBorder](#getborder)|현재 페이저 컨트롤의 테두리 크기를 검색합니다.|  
|[CPagerCtrl::GetButtonSize](#getbuttonsize)|현재 페이저 컨트롤의 단추 크기를 검색합니다.|  
|[CPagerCtrl::GetButtonState](#getbuttonstate)|현재 페이저 컨트롤에서 지정 된 단추의 상태를 검색합니다.|  
|[CPagerCtrl::GetDropTarget](#getdroptarget)|검색 된 [IDropTarget](http://msdn.microsoft.com/library/windows/desktop/ms679679) 현재 페이저 컨트롤에 대 한 인터페이스입니다.|  
|[CPagerCtrl::GetScrollPos](#getscrollpos)|현재 페이저 컨트롤의 스크롤 위치를 검색합니다.|  
|[CPagerCtrl::IsButtonDepressed](#isbuttondepressed)|현재 페이저 컨트롤의 지정 된 단추 인지 여부를 나타냅니다 `pressed` 상태입니다.|  
|[CPagerCtrl::IsButtonGrayed](#isbuttongrayed)|현재 페이저 컨트롤의 지정 된 단추 인지 여부를 나타냅니다 `grayed` 상태입니다.|  
|[CPagerCtrl::IsButtonHot](#isbuttonhot)|현재 페이저 컨트롤의 지정 된 단추 인지 여부를 나타냅니다 `hot` 상태입니다.|  
|[CPagerCtrl::IsButtonInvisible](#isbuttoninvisible)|현재 페이저 컨트롤의 지정 된 단추 인지 여부를 나타냅니다 `invisible` 상태입니다.|  
|[CPagerCtrl::IsButtonNormal](#isbuttonnormal)|현재 페이저 컨트롤의 지정 된 단추 인지 여부를 나타냅니다 `normal` 상태입니다.|  
|[CPagerCtrl::RecalcSize](#recalcsize)|현재 호출기 컨트롤이 포함 된 창의 크기 다시 계산 하도록 합니다.|  
|[CPagerCtrl::SetBkColor](#setbkcolor)|현재 페이저 컨트롤의 배경색을 설정합니다.|  
|[CPagerCtrl::SetBorder](#setborder)|현재 페이저 컨트롤의 테두리 크기를 설정합니다.|  
|[CPagerCtrl::SetButtonSize](#setbuttonsize)|현재 페이저 컨트롤의 단추 크기를 설정합니다.|  
|[CPagerCtrl::SetChild](#setchild)|현재 페이저 컨트롤에 포함 된 창을 설정입니다.|  
|[CPagerCtrl::SetScrollPos](#setscrollpos)|현재 페이저 컨트롤의 스크롤 위치를 설정합니다.|  
  
## <a name="remarks"></a>주의  
 호출기 컨트롤이 선형 및 포함 하 고 창 보다 더 큰 포함 된 창을 보기로 스크롤할 수 있게 하는 다른 창을 포함 하는 창입니다. 페이저 컨트롤 자동으로 해당 가장 멀리 있는 범위에 포함 된 창은 스크롤될 때 사라진 두 스크롤 단추를 표시 하 고 그렇지 않으면 다시 나타납니다. 가로 또는 세로로 스크롤 하는 페이저 컨트롤을 만들 수 있습니다.  
  
 예를 들어, 응용 프로그램에 해당 항목이 모두 표시 하기에 충분 하지 않은 경우 도구 모음, 페이저 컨트롤에 도구 모음을 지정할 수 있습니다 및 사용자는 왼쪽 또는 오른쪽의 모든 항목에 액세스 하 고 도구 모음을 스크롤할 수 있습니다. Microsoft Internet Explorer 버전 4.0 (commctrl.dll 버전 4.71) 페이저 컨트롤을 소개 합니다.  
  
 `CPagerCtrl` 에서 파생 된 클래스는 [CWnd](../../mfc/reference/cwnd-class.md) 클래스입니다. 자세한 내용 및 pager 컨트롤의 그림에 대 한 참조 [페이저 컨트롤](http://msdn.microsoft.com/library/windows/desktop/bb760855)합니다.  
  
## <a name="inheritance-hierarchy"></a>상속 계층  
 [CObject](../../mfc/reference/cobject-class.md)  
  
 [CCmdTarget](../../mfc/reference/ccmdtarget-class.md)  
  
 [CWnd](../../mfc/reference/cwnd-class.md)  
  
 `CPagerCtrl`  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** afxcmn.h  
  
##  <a name="cpagerctrl"></a>CPagerCtrl::CPagerCtrl  
 `CPagerCtrl` 개체를 생성합니다.  
  
```  
CPagerCtrl();
```  
  
### <a name="remarks"></a>주의  
 사용 된 [CPagerCtrl::Create](#create) 또는 [CPagerCtrl::CreateEx](#createex) 페이저 컨트롤을 만들고에 연결 하는 메서드는 `CPagerCtrl` 개체입니다.  
  
##  <a name="create"></a>CPagerCtrl::Create  
 지정 된 스타일으로 페이저 컨트롤을 만들고 현재 연결 `CPagerCtrl` 개체입니다.  
  
```  
virtual BOOL Create(
    DWORD dwStyle,   
    const RECT& rect,   
    CWnd* pParentWnd,   
    UINT nID);
```  
  
### <a name="parameters"></a>매개 변수  
  
|매개 변수|설명|  
|---------------|-----------------|  
|[in] `dwStyle`|비트 조합 (OR) [창 스타일](../../mfc/reference/window-styles.md) 및 [페이저 컨트롤 스타일](http://msdn.microsoft.com/library/windows/desktop/bb760859) 컨트롤에 적용할 수 있습니다.|  
|[in] `rect`|에 대 한 참조는 [RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897) 클라이언트 좌표에서 컨트롤의 크기와 위치를 포함 하는 구조입니다.|  
|[in] `pParentWnd`|에 대 한 포인터는 [CWnd](../../mfc/reference/cwnd-class.md) 개체 컨트롤의 부모 창입니다. 이 매개 변수 수 없습니다 `NULL`합니다.|  
|[in] `nID`|컨트롤의 ID입니다.|  
  
### <a name="return-value"></a>반환 값  
 이 메서드가 성공적으로 수행되면 `true`이고, 그렇지 않으면 `false`입니다.  
  
### <a name="remarks"></a>주의  
 페이저 컨트롤을 만들려면 선언는 `CPagerCtrl` 변수를 다음 호출에서 [CPagerCtrl::Create](#create) 또는 [CPagerCtrl::CreateEx](#createex) 변수에 메서드.  
  
### <a name="example"></a>예제  
 다음 예제에서는 페이저 컨트롤을 만들어 다음 사용 하는 [CPagerCtrl::SetChild](#setchild) 페이저 컨트롤에서 매우 긴 단추 컨트롤을 연결 하는 방법이 있습니다. 사용 하 여는 [CPagerCtrl::SetButtonSize](#setbuttonsize) 20 픽셀 페이저 컨트롤의 높이 설정 하는 메서드 및 [CPagerCtrl::SetBorder](#setborder) 1 픽셀로 테두리 두께 설정 하는 방법입니다.  
  
 [!code-cpp[NVC_MFC_CSplitButton_s&#2;&1;](../../mfc/reference/codesnippet/cpp/cpagerctrl-class_1.cpp)]  
  
##  <a name="createex"></a>CPagerCtrl::CreateEx  
 확장된 스타일을 지정된 하 여 페이저 컨트롤을 만들고 현재 연결 `CPagerCtrl` 개체입니다.  
  
```  
virtual BOOL CreateEx(
    DWORD dwExStyle,   
    DWORD dwStyle,   
    const RECT& rect,   
    CWnd* pParentWnd,   
    UINT nID);
```  
  
### <a name="parameters"></a>매개 변수  
  
|매개 변수|설명|  
|---------------|-----------------|  
|[in] `dwExStyle`|확장된 스타일을 컨트롤에 적용할 수의 비트 조합입니다. 자세한 내용은 참조는 `dwExStyle` 의 매개 변수는 [CreateWindowEx](http://msdn.microsoft.com/library/windows/desktop/ms632680) 함수입니다.|  
|[in] `dwStyle`|비트 조합 (OR) [창 스타일](../../mfc/reference/window-styles.md) 및 [페이저 컨트롤 스타일](http://msdn.microsoft.com/library/windows/desktop/bb760859) 컨트롤에 적용할 수 있습니다.|  
|[in] `rect`|에 대 한 참조는 [RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897) 클라이언트 좌표에서 컨트롤의 크기와 위치를 포함 하는 구조입니다.|  
|[in] `pParentWnd`|에 대 한 포인터는 [CWnd](../../mfc/reference/cwnd-class.md) 개체 컨트롤의 부모 창입니다. 이 매개 변수 수 없습니다 `NULL`합니다.|  
|[in] `nID`|컨트롤의 ID입니다.|  
  
### <a name="return-value"></a>반환 값  
 이 메서드가 성공적으로 수행되면 `true`이고, 그렇지 않으면 `false`입니다.  
  
### <a name="remarks"></a>주의  
 페이저 컨트롤을 만들려면 선언는 `CPagerCtrl` 변수를 다음 호출에서 [CPagerCtrl::Create](#create) 또는 [CPagerCtrl::CreateEx](#createex) 변수에 메서드.  
  
##  <a name="forwardmouse"></a>CPagerCtrl::ForwardMouse  
 설정 하거나 해제 전달 [WM_MOUSEMOVE](http://msdn.microsoft.com/library/windows/desktop/ms645616) 메시지는 현재 페이저 컨트롤에 포함 된 창입니다.  
  
```  
void ForwardMouse(BOOL bForward);
```  
  
### <a name="parameters"></a>매개 변수  
  
|매개 변수|설명|  
|---------------|-----------------|  
|[in] `bForward`|`true`마우스 메시지 전달 또는 `false` 마우스 메시지를 전달 하지 않습니다.|  
  
### <a name="remarks"></a>주의  
 이 메서드는 전송 된 [PGM_FORWARDMOUSE](http://msdn.microsoft.com/library/windows/desktop/bb760867) 에 설명 된 메시지는 [!INCLUDE[winSDK](../../atl/includes/winsdk_md.md)]합니다.  
  
##  <a name="getborder"></a>CPagerCtrl::GetBorder  
 현재 페이저 컨트롤의 테두리 크기를 검색합니다.  
  
```  
int GetBorder() const;  
```  
  
### <a name="return-value"></a>반환 값  
 현재 테두리 두께 픽셀 단위로 지정 합니다.  
  
### <a name="remarks"></a>주의  
 이 메서드는 전송 된 [PGM_GETBORDER](http://msdn.microsoft.com/library/windows/desktop/bb760869) 에 설명 된 메시지는 [!INCLUDE[winSDK](../../atl/includes/winsdk_md.md)]합니다.  
  
### <a name="example"></a>예제  
 다음 예제에서는 [CPagerCtrl::GetBorder](#getborder) 페이저 컨트롤의 테두리의 두께 검색 하는 메서드입니다.  
  
 [!code-cpp[NVC_MFC_CSplitButton_s&#2;&5;](../../mfc/reference/codesnippet/cpp/cpagerctrl-class_2.cpp)]  
  
##  <a name="getbkcolor"></a>CPagerCtrl::GetBkColor  
 현재 페이저 컨트롤의 배경색을 검색합니다.  
  
```  
COLORREF GetBkColor() const;  
```  
  
### <a name="return-value"></a>반환 값  
 A [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449) 페이저 컨트롤의 현재 배경색을 포함 하는 값입니다.  
  
### <a name="remarks"></a>주의  
 이 메서드는 전송 된 [PGM_GETBKCOLOR](http://msdn.microsoft.com/library/windows/desktop/bb760868) 에 설명 된 메시지는 [!INCLUDE[winSDK](../../atl/includes/winsdk_md.md)]합니다.  
  
### <a name="example"></a>예제  
 다음 예제에서는 [CPagerCtrl::SetBkColor](#setbkcolor) 빨간색으로 페이저 컨트롤의 배경색을 설정 하는 메서드 및 [CPagerCtrl::GetBkColor](#getbkcolor) 변경을 수행 했는지 확인 하는 방법입니다.  
  
 [!code-cpp[NVC_MFC_CSplitButton_s&#2;&4;](../../mfc/reference/codesnippet/cpp/cpagerctrl-class_3.cpp)]  
  
##  <a name="getbuttonsize"></a>CPagerCtrl::GetButtonSize  
 현재 페이저 컨트롤의 단추 크기를 검색합니다.  
  
```  
int GetButtonSize() const;  
```  
  
### <a name="return-value"></a>반환 값  
 현재 단추 크기를 픽셀 단위로 지정 합니다.  
  
### <a name="remarks"></a>주의  
 이 메서드는 전송 된 [PGM_GETBUTTONSIZE](http://msdn.microsoft.com/library/windows/desktop/bb760870) 에 설명 된 메시지는 [!INCLUDE[winSDK](../../atl/includes/winsdk_md.md)]합니다.  
  
 페이저 컨트롤에는 `PGS_HORZ` 페이저 단추의 너비를 결정 하는 스타일을 단추 크기가 고 페이저 컨트롤에는 `PGS_VERT` 스타일을 단추 크기 페이저 단추의 높이 결정 합니다. 자세한 내용은 참조 [페이저 컨트롤 스타일](http://msdn.microsoft.com/library/windows/desktop/bb760859)합니다.  
  
##  <a name="getbuttonstate"></a>CPagerCtrl::GetButtonState  
 현재 페이저 컨트롤에서 지정한 스크롤 단추의 상태를 검색합니다.  
  
```  
DWORD GetButtonState(int iButton) const;  
```  
  
### <a name="parameters"></a>매개 변수  
  
|매개 변수|설명|  
|---------------|-----------------|  
|[in] `iButton`|상태를 검색할 단추를 나타냅니다. 페이저 컨트롤 스타일이 경우 `PGS_HORZ`, 지정 `PGB_TOPORLEFT` 왼쪽된 단추에 대 한 고 `PGB_BOTTOMORRIGHT` 오른쪽의 단추에 대 한 합니다. 페이저 컨트롤 스타일이 경우 `PGS_VERT`, 지정 `PGB_TOPORLEFT` 위쪽 단추에 대 한 고 `PGB_BOTTOMORRIGHT` 아래쪽 단추에 대 한 합니다. 자세한 내용은 참조 [페이저 컨트롤 스타일](http://msdn.microsoft.com/library/windows/desktop/bb760859)합니다.|  
  
### <a name="return-value"></a>반환 값  
 지정 된 단추의 상태는 `iButton` 매개 변수입니다. The state is either `PGF_INVISIBLE`, `PGF_NORMAL`, `PGF_GRAYED`, `PGF_DEPRESSED`, or `PGF_HOT`. 자세한 내용은 반환 값 섹션을 참조는 [PGM_GETBUTTONSTATE](http://msdn.microsoft.com/library/windows/desktop/bb760871) 메시지입니다.  
  
### <a name="remarks"></a>주의  
 이 메서드는 전송 된 [PGM_GETBUTTONSTATE](http://msdn.microsoft.com/library/windows/desktop/bb760871) 에 설명 된 메시지는 [!INCLUDE[winSDK](../../atl/includes/winsdk_md.md)]합니다.  
  
##  <a name="getdroptarget"></a>CPagerCtrl::GetDropTarget  
 검색 된 [IDropTarget](http://msdn.microsoft.com/library/windows/desktop/ms679679) 현재 페이저 컨트롤에 대 한 인터페이스입니다.  
  
```  
IDropTarget* GetDropTarget() const;  
```  
  
### <a name="return-value"></a>반환 값  
 에 대 한 포인터는 `IDropTarget` 현재 페이저 컨트롤에 대 한 인터페이스입니다.  
  
### <a name="remarks"></a>주의  
 `IDropTarget`구현 하는 인터페이스 중 하나는 응용 프로그램에서 끌어서 놓기 작업을 지원 합니다.  
  
 이 메서드는 전송 된 [PGM_GETDROPTARGET](http://msdn.microsoft.com/library/windows/desktop/bb760872) 에 설명 된 메시지는 [!INCLUDE[winSDK](../../atl/includes/winsdk_md.md)]합니다. 이 메서드의 호출자는 호출을 담당는 `Release` 의 멤버는 [IDropTarget](http://msdn.microsoft.com/library/windows/desktop/ms679679) 인터페이스는 인터페이스는 더 이상 필요 합니다.  
  
##  <a name="getscrollpos"></a>CPagerCtrl::GetScrollPos  
 현재 페이저 컨트롤의 스크롤 위치를 검색합니다.  
  
```  
int GetScrollPos() const;  
```  
  
### <a name="return-value"></a>반환 값  
 현재 스크롤 위치를 픽셀 단위로 지정 합니다.  
  
### <a name="remarks"></a>주의  
 이 메서드는 전송 된 [PGM_GETPOS](http://msdn.microsoft.com/library/windows/desktop/bb760874) 에 설명 된 메시지는 [!INCLUDE[winSDK](../../atl/includes/winsdk_md.md)]합니다.  
  
### <a name="example"></a>예제  
 다음 예제에서는 [CPagerCtrl::GetScrollPos](#getscrollpos) 페이저 컨트롤의 현재 스크롤 위치를 검색 하는 메서드입니다. 이 예제에서는 사용 하는 페이저 컨트롤을&0;으로 맨 왼쪽 위치 이미 스크롤되지 않는 경우는 [CPagerCtrl::SetScrollPos](#setscrollpos) 스크롤 위치를&0;으로 설정 하는 방법입니다.  
  
 [!code-cpp[NVC_MFC_CSplitButton_s&#2;&7;](../../mfc/reference/codesnippet/cpp/cpagerctrl-class_4.cpp)]  
  
##  <a name="isbuttondepressed"></a>CPagerCtrl::IsButtonDepressed  
 현재 페이저 컨트롤의 지정 된 스크롤 단추를 눌렀는지 여부를 나타냅니다.  
  
```  
BOOL IsButtonDepressed(int iButton) const;  
```  
  
### <a name="parameters"></a>매개 변수  
  
|매개 변수|설명|  
|---------------|-----------------|  
|[in] `iButton`|상태를 검색할 단추를 나타냅니다. 페이저 컨트롤 스타일이 경우 `PGS_HORZ`, 지정 `PGB_TOPORLEFT` 왼쪽된 단추에 대 한 고 `PGB_BOTTOMORRIGHT` 오른쪽의 단추에 대 한 합니다. 페이저 컨트롤 스타일이 경우 `PGS_VERT`, 지정 `PGB_TOPORLEFT` 위쪽 단추에 대 한 고 `PGB_BOTTOMORRIGHT` 아래쪽 단추에 대 한 합니다. 자세한 내용은 참조 [페이저 컨트롤 스타일](http://msdn.microsoft.com/library/windows/desktop/bb760859)합니다.|  
  
### <a name="return-value"></a>반환 값  
 `true`지정 된 단추를 누른 상태 이면 그렇지 않으면 `false`합니다.  
  
### <a name="remarks"></a>주의  
 이 메서드는 전송 된 [PGM_GETBUTTONSTATE](http://msdn.microsoft.com/library/windows/desktop/bb760871) 에 설명 된 메시지는 [!INCLUDE[winSDK](../../atl/includes/winsdk_md.md)]합니다. 반환 되는 상태 인지를 테스트 하는 다음 `PGF_DEPRESSED`합니다. 자세한 내용은 반환 값 섹션을 참조는 [PGM_GETBUTTONSTATE](http://msdn.microsoft.com/library/windows/desktop/bb760871) 메시지입니다.  
  
##  <a name="isbuttongrayed"></a>CPagerCtrl::IsButtonGrayed  
 지정된 된 스크롤 단추는 현재 페이저 컨트롤의 회색으로 표시 된 상태 인지 여부를 나타냅니다.  
  
```  
BOOL IsButtonGrayed(int iButton) const;  
```  
  
### <a name="parameters"></a>매개 변수  
  
|매개 변수|설명|  
|---------------|-----------------|  
|[in] `iButton`|상태를 검색할 단추를 나타냅니다. 페이저 컨트롤 스타일이 경우 `PGS_HORZ`, 지정 `PGB_TOPORLEFT` 왼쪽된 단추에 대 한 고 `PGB_BOTTOMORRIGHT` 오른쪽의 단추에 대 한 합니다. 페이저 컨트롤 스타일이 경우 `PGS_VERT`, 지정 `PGB_TOPORLEFT` 위쪽 단추에 대 한 고 `PGB_BOTTOMORRIGHT` 아래쪽 단추에 대 한 합니다. 자세한 내용은 참조 [페이저 컨트롤 스타일](http://msdn.microsoft.com/library/windows/desktop/bb760859)합니다.|  
  
### <a name="return-value"></a>반환 값  
 `true`지정 된 단추가 회색으로 표시 된 상태 이면 경우 그렇지 않으면 `false`합니다.  
  
### <a name="remarks"></a>주의  
 이 메서드는 전송 된 [PGM_GETBUTTONSTATE](http://msdn.microsoft.com/library/windows/desktop/bb760871) 에 설명 된 메시지는 [!INCLUDE[winSDK](../../atl/includes/winsdk_md.md)]합니다. 반환 되는 상태 인지를 테스트 하는 다음 `PGF_GRAYED`합니다. 자세한 내용은 반환 값 섹션을 참조는 [PGM_GETBUTTONSTATE](http://msdn.microsoft.com/library/windows/desktop/bb760871) 메시지입니다.  
  
##  <a name="isbuttonhot"></a>CPagerCtrl::IsButtonHot  
 지정된 된 스크롤 단추는 현재 페이저 컨트롤의 활성 상태 인지 여부를 나타냅니다.  
  
```  
BOOL IsButtonHot(int iButton) const;  
```  
  
### <a name="parameters"></a>매개 변수  
  
|매개 변수|설명|  
|---------------|-----------------|  
|[in] `iButton`|상태를 검색할 단추를 나타냅니다. 페이저 컨트롤 스타일이 경우 `PGS_HORZ`, 지정 `PGB_TOPORLEFT` 왼쪽된 단추에 대 한 고 `PGB_BOTTOMORRIGHT` 오른쪽의 단추에 대 한 합니다. 페이저 컨트롤 스타일이 경우 `PGS_VERT`, 지정 `PGB_TOPORLEFT` 위쪽 단추에 대 한 고 `PGB_BOTTOMORRIGHT` 아래쪽 단추에 대 한 합니다. 자세한 내용은 참조 [페이저 컨트롤 스타일](http://msdn.microsoft.com/library/windows/desktop/bb760859)합니다.|  
  
### <a name="return-value"></a>반환 값  
 `true`지정한 단추의; 활성 상태의 경우 그렇지 않으면 `false`합니다.  
  
### <a name="remarks"></a>주의  
 이 메서드는 전송 된 [PGM_GETBUTTONSTATE](http://msdn.microsoft.com/library/windows/desktop/bb760871) 에 설명 된 메시지는 [!INCLUDE[winSDK](../../atl/includes/winsdk_md.md)]합니다. 반환 되는 상태 인지를 테스트 하는 다음 `PGF_HOT`합니다. 자세한 내용은 반환 값 섹션을 참조는 [PGM_GETBUTTONSTATE](http://msdn.microsoft.com/library/windows/desktop/bb760871) 메시지입니다.  
  
##  <a name="isbuttoninvisible"></a>CPagerCtrl::IsButtonInvisible  
 현재 페이저 컨트롤의 지정한 스크롤 단추 보이지 않는 상태 인지 여부를 나타냅니다.  
  
```  
BOOL IsButtonInvisible(int iButton) const;  
```  
  
### <a name="parameters"></a>매개 변수  
  
|매개 변수|설명|  
|---------------|-----------------|  
|[in] `iButton`|상태를 검색할 단추를 나타냅니다. 페이저 컨트롤 스타일이 경우 `PGS_HORZ`, 지정 `PGB_TOPORLEFT` 왼쪽된 단추에 대 한 고 `PGB_BOTTOMORRIGHT` 오른쪽의 단추에 대 한 합니다. 페이저 컨트롤 스타일이 경우 `PGS_VERT`, 지정 `PGB_TOPORLEFT` 위쪽 단추에 대 한 고 `PGB_BOTTOMORRIGHT` 아래쪽 단추에 대 한 합니다. 자세한 내용은 참조 [페이저 컨트롤 스타일](http://msdn.microsoft.com/library/windows/desktop/bb760859)합니다.|  
  
### <a name="return-value"></a>반환 값  
 `true`보이지 않는 상태 이면 지정 된 단추를 그렇지 않으면 `false`합니다.  
  
### <a name="remarks"></a>주의  
 Windows에서는 추가 단추를 클릭 하면 없습니다 포함 된 창의 더 뷰로 가져올 때문에 가장 멀리 있는 범위에 포함 된 창은 스크롤될 때 특정 방향으로 스크롤 단추는 표시 되지 않습니다.  
  
 이 메서드는 전송 된 [PGM_GETBUTTONSTATE](http://msdn.microsoft.com/library/windows/desktop/bb760871) 에 설명 된 메시지는 [!INCLUDE[winSDK](../../atl/includes/winsdk_md.md)]합니다. 반환 되는 상태 인지를 테스트 하는 다음 `PGF_INVISIBLE`합니다. 자세한 내용은 반환 값 섹션을 참조는 [PGM_GETBUTTONSTATE](http://msdn.microsoft.com/library/windows/desktop/bb760871) 메시지입니다.  
  
### <a name="example"></a>예제  
 다음 예제에서는 [CPagerCtrl::IsButtonInvisible](#isbuttoninvisible) 페이저 컨트롤의 왼쪽 및 오른쪽 스크롤 단추는 표시 여부를 확인 하 합니다.  
  
 [!code-cpp[NVC_MFC_CSplitButton_s&#2;&6;](../../mfc/reference/codesnippet/cpp/cpagerctrl-class_5.cpp)]  
  
##  <a name="isbuttonnormal"></a>CPagerCtrl::IsButtonNormal  
 지정된 된 스크롤 단추는 현재 페이저 컨트롤의 정상 상태 인지 여부를 나타냅니다.  
  
```  
BOOL IsButtonNormal(int iButton) const;  
```  
  
### <a name="parameters"></a>매개 변수  
  
|매개 변수|설명|  
|---------------|-----------------|  
|[in] `iButton`|상태를 검색할 단추를 나타냅니다. 페이저 컨트롤 스타일이 경우 `PGS_HORZ`, 지정 `PGB_TOPORLEFT` 왼쪽된 단추에 대 한 고 `PGB_BOTTOMORRIGHT` 오른쪽의 단추에 대 한 합니다. 페이저 컨트롤 스타일이 경우 `PGS_VERT`, 지정 `PGB_TOPORLEFT` 위쪽 단추에 대 한 고 `PGB_BOTTOMORRIGHT` 아래쪽 단추에 대 한 합니다. 자세한 내용은 참조 [페이저 컨트롤 스타일](http://msdn.microsoft.com/library/windows/desktop/bb760859)합니다.|  
  
### <a name="return-value"></a>반환 값  
 `true`정상 상태 이면 지정 된 단추를 그렇지 않으면 `false`합니다.  
  
### <a name="remarks"></a>주의  
 이 메서드는 전송 된 [PGM_GETBUTTONSTATE](http://msdn.microsoft.com/library/windows/desktop/bb760871) 에 설명 된 메시지는 [!INCLUDE[winSDK](../../atl/includes/winsdk_md.md)]합니다. 반환 되는 상태 인지를 테스트 하는 다음 `PGF_NORMAL`합니다. 자세한 내용은 반환 값 섹션을 참조는 [PGM_GETBUTTONSTATE](http://msdn.microsoft.com/library/windows/desktop/bb760871) 메시지입니다.  
  
##  <a name="recalcsize"></a>CPagerCtrl::RecalcSize  
 현재 호출기 컨트롤이 포함 된 창의 크기 다시 계산 하도록 합니다.  
  
```  
void RecalcSize();
```  
  
### <a name="remarks"></a>주의  
 이 메서드는 전송 된 [PGM_RECALCSIZE](http://msdn.microsoft.com/library/windows/desktop/bb760876) 에 설명 된 메시지는 [!INCLUDE[winSDK](../../atl/includes/winsdk_md.md)]합니다. 따라서 페이저 컨트롤 보냅니다는 [PGN_CALCSIZE](http://msdn.microsoft.com/library/windows/desktop/bb760864) 는 스크롤 가능한 창 크기에 포함 된 알림을 합니다.  
  
### <a name="example"></a>예제  
 다음 예제에서는 [CPagerCtrl::RecalcSize](#recalcsize) 메서드를 현재 페이저 컨트롤 크기 다시 계산을 요청 합니다.  
  
 [!code-cpp[NVC_MFC_CSplitButton_s&#2;&3;](../../mfc/reference/codesnippet/cpp/cpagerctrl-class_6.cpp)]  
  
### <a name="example"></a>예제  
 다음 예제에서는 [리플렉션 메시지](../../mfc/tn062-message-reflection-for-windows-controls.md) 페이저 컨트롤 크기 계산을 수행 하는 컨트롤의 부모 대화 하도록 하는 대신 다시 계산을 사용할 수 있도록 합니다. 예제에서는 파생 되는 `MyPagerCtrl` 에서 클래스는 [CPagerCtrl 클래스](../../mfc/reference/cpagerctrl-class.md), 다음 메시지 지도 사용 하 여 연결 하는 [PGN_CALCSIZE](http://msdn.microsoft.com/library/windows/desktop/bb760864) 알림을 `OnCalcsize` 알림 처리기. 이 예제에서는 알림 처리기를 고정된 값 페이저 컨트롤의 높이 너비를 설정합니다.  
  
 [!code-cpp[NVC_MFC_CSplitButton_s&#2;&8;](../../mfc/reference/codesnippet/cpp/cpagerctrl-class_7.cpp)]  
  
##  <a name="setbkcolor"></a>CPagerCtrl::SetBkColor  
 현재 페이저 컨트롤의 배경색을 설정합니다.  
  
```  
COLORREF SetBkColor(COLORREF clrBk);
```  
  
### <a name="parameters"></a>매개 변수  
  
|매개 변수|설명|  
|---------------|-----------------|  
|[in] `clrBk`|A [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449) 새 배경 색 페이저 컨트롤을 포함 하는 값입니다.|  
  
### <a name="return-value"></a>반환 값  
 A [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449) 페이저 컨트롤의 이전 배경색을 포함 하는 값입니다.  
  
### <a name="remarks"></a>주의  
 이 메서드는 전송 된 [PGM_SETBKCOLOR](http://msdn.microsoft.com/library/windows/desktop/bb760878) 에 설명 된 메시지는 [!INCLUDE[winSDK](../../atl/includes/winsdk_md.md)]합니다.  
  
### <a name="example"></a>예제  
 다음 예제에서는 [CPagerCtrl::SetBkColor](#setbkcolor) 빨간색으로 페이저 컨트롤의 배경색을 설정 하는 메서드 및 [CPagerCtrl::GetBkColor](#getbkcolor) 변경을 수행 했는지 확인 하는 방법입니다.  
  
 [!code-cpp[NVC_MFC_CSplitButton_s&#2;&4;](../../mfc/reference/codesnippet/cpp/cpagerctrl-class_3.cpp)]  
  
##  <a name="setborder"></a>CPagerCtrl::SetBorder  
 현재 페이저 컨트롤의 테두리 크기를 설정합니다.  
  
```  
int SetBorder(int iBorder);
```  
  
### <a name="parameters"></a>매개 변수  
  
|매개 변수|설명|  
|---------------|-----------------|  
|[in] `iBorder`|새 테두리 두께 픽셀 단위로 지정 합니다. 하는 경우는 `iBorder` 매개 변수가 음수 이면 테두리 크기는&0;으로 설정 됩니다.|  
  
### <a name="return-value"></a>반환 값  
 이전 테두리 두께 픽셀 단위로 지정 합니다.  
  
### <a name="remarks"></a>주의  
 이 메서드는 전송 된 [PGM_SETBORDER](http://msdn.microsoft.com/library/windows/desktop/bb760880) 에 설명 된 메시지는 [!INCLUDE[winSDK](../../atl/includes/winsdk_md.md)]합니다.  
  
### <a name="example"></a>예제  
 다음 예제에서는 페이저 컨트롤을 만들어 다음 사용 하는 [CPagerCtrl::SetChild](#setchild) 페이저 컨트롤에서 매우 긴 단추 컨트롤을 연결 하는 방법이 있습니다. 사용 하 여는 [CPagerCtrl::SetButtonSize](#setbuttonsize) 20 픽셀 페이저 컨트롤의 높이 설정 하는 메서드 및 [CPagerCtrl::SetBorder](#setborder) 1 픽셀로 테두리 두께 설정 하는 방법입니다.  
  
 [!code-cpp[NVC_MFC_CSplitButton_s&#2;&1;](../../mfc/reference/codesnippet/cpp/cpagerctrl-class_1.cpp)]  
  
##  <a name="setbuttonsize"></a>CPagerCtrl::SetButtonSize  
 현재 페이저 컨트롤의 단추 크기를 설정합니다.  
  
```  
int SetButtonSize(int iButtonSize);
```  
  
### <a name="parameters"></a>매개 변수  
  
|매개 변수|설명|  
|---------------|-----------------|  
|[in] `iButtonSize`|새 단추 크기를 픽셀 단위로 지정 합니다.|  
  
### <a name="return-value"></a>반환 값  
 이전 단추 크기를 픽셀 단위로 지정 합니다.  
  
### <a name="remarks"></a>주의  
 이 메서드는 전송 된 [PGM_SETBUTTONSIZE](http://msdn.microsoft.com/library/windows/desktop/bb760886) 에 설명 된 메시지는 [!INCLUDE[winSDK](../../atl/includes/winsdk_md.md)]합니다.  
  
 페이저 컨트롤에는 `PGS_HORZ` 페이저 단추의 너비를 결정 하는 스타일을 단추 크기가 고 페이저 컨트롤에는 `PGS_VERT` 스타일을 단추 크기 페이저 단추의 높이 결정 합니다. 기본 단추 크기는 3-4의 스크롤 막대의 너비 및 최소 단추 크기는 12 픽셀입니다. 자세한 내용은 참조 [페이저 컨트롤 스타일](http://msdn.microsoft.com/library/windows/desktop/bb760859)합니다.  
  
### <a name="example"></a>예제  
 다음 예제에서는 페이저 컨트롤을 만들어 다음 사용 하는 [CPagerCtrl::SetChild](#setchild) 페이저 컨트롤에서 매우 긴 단추 컨트롤을 연결 하는 방법이 있습니다. 사용 하 여는 [CPagerCtrl::SetButtonSize](#setbuttonsize) 20 픽셀 페이저 컨트롤의 높이 설정 하는 메서드 및 [CPagerCtrl::SetBorder](#setborder) 1 픽셀로 테두리 두께 설정 하는 방법입니다.  
  
 [!code-cpp[NVC_MFC_CSplitButton_s&#2;&1;](../../mfc/reference/codesnippet/cpp/cpagerctrl-class_1.cpp)]  
  
##  <a name="setchild"></a>CPagerCtrl::SetChild  
 현재 페이저 컨트롤에 포함 된 창을 설정입니다.  
  
```  
void SetChild(HWND hwndChild);
```  
  
### <a name="parameters"></a>매개 변수  
  
|매개 변수|설명|  
|---------------|-----------------|  
|[in] `hwndChild`|포함 된 창을 처리 합니다.|  
  
### <a name="remarks"></a>주의  
 이 메서드는 전송 된 [PGM_SETCHILD](http://msdn.microsoft.com/library/windows/desktop/bb760884) 에 설명 된 메시지는 [!INCLUDE[winSDK](../../atl/includes/winsdk_md.md)]합니다.  
  
 이 메서드는 포함 된 창;의 부모를 변경 하지 않습니다. 만 스크롤에 대 한 페이저 컨트롤에 대 한 창 핸들을 할당합니다. 대부분의 경우에서 포함 된 창은 페이저 컨트롤의 자식 창이 됩니다.  
  
### <a name="example"></a>예제  
 다음 예제에서는 페이저 컨트롤을 만들어 다음 사용 하는 [CPagerCtrl::SetChild](#setchild) 페이저 컨트롤에서 매우 긴 단추 컨트롤을 연결 하는 방법이 있습니다. 사용 하 여는 [CPagerCtrl::SetButtonSize](#setbuttonsize) 20 픽셀 페이저 컨트롤의 높이 설정 하는 메서드 및 [CPagerCtrl::SetBorder](#setborder) 1 픽셀로 테두리 두께 설정 하는 방법입니다.  
  
 [!code-cpp[NVC_MFC_CSplitButton_s&#2;&1;](../../mfc/reference/codesnippet/cpp/cpagerctrl-class_1.cpp)]  
  
##  <a name="setscrollpos"></a>CPagerCtrl::SetScrollPos  
 현재 페이저 컨트롤의 스크롤 위치를 설정합니다.  
  
```  
void SetScrollPos(int iPos);
```  
  
### <a name="parameters"></a>매개 변수  
  
|매개 변수|설명|  
|---------------|-----------------|  
|[in] `iPos`|새 스크롤 위치를 픽셀 단위로 지정 합니다.|  
  
### <a name="remarks"></a>주의  
 이 메서드는 전송 된 [PGM_SETPOS](http://msdn.microsoft.com/library/windows/desktop/bb760886) 에 설명 된 메시지는 [!INCLUDE[winSDK](../../atl/includes/winsdk_md.md)]합니다.  
  
## <a name="see-also"></a>참고 항목  
 [CPagerCtrl 클래스](../../mfc/reference/cpagerctrl-class.md)   
 [계층 구조 차트](../../mfc/hierarchy-chart.md)   
 [페이저 컨트롤](http://msdn.microsoft.com/library/windows/desktop/bb760855)



