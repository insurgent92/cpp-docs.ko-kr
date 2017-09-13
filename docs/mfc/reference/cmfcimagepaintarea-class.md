---
title: "CMFCImagePaintArea 클래스 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- CMFCImagePaintArea
- AFXIMAGEPAINTAREA/CMFCImagePaintArea
- AFXIMAGEPAINTAREA/CMFCImagePaintArea::CMFCImagePaintArea
- AFXIMAGEPAINTAREA/CMFCImagePaintArea::GetMode
- AFXIMAGEPAINTAREA/CMFCImagePaintArea::SetBitmap
- AFXIMAGEPAINTAREA/CMFCImagePaintArea::SetColor
- AFXIMAGEPAINTAREA/CMFCImagePaintArea::SetMode
dev_langs:
- C++
helpviewer_keywords:
- CMFCImagePaintArea class
ms.assetid: c59eec22-f15a-4e58-8c4d-4a18a41f4452
caps.latest.revision: 21
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
ms.openlocfilehash: c16fd9605474e57f167646ddc9bc91d235d1cba5
ms.contentlocale: ko-kr
ms.lasthandoff: 02/24/2017

---
# <a name="cmfcimagepaintarea-class"></a>CMFCImagePaintArea 클래스
이미지 편집기 대화 상자에 이미지를 수정 하는 데 사용할 수 있는 그림 영역을 제공 합니다.  
  
## <a name="syntax"></a>구문  
  
```  
class CMFCImagePaintArea : public CButton  
```  
  
## <a name="members"></a>멤버  
  
### <a name="public-constructors"></a>Public 생성자  
  
|||  
|-|-|  
|이름|설명|  
|[CMFCImagePaintArea::CMFCImagePaintArea](#cmfcimagepaintarea)|`CMFCImagePaintArea` 개체를 생성합니다.|  
|`CMFCImagePaintArea::~CMFCImagePaintArea`|소멸자|  
  
### <a name="public-methods"></a>Public 메서드  
  
|||  
|-|-|  
|이름|설명|  
|[CMFCImagePaintArea::GetMode](#getmode)|현재 그리기 모드를 검색합니다.|  
|[CMFCImagePaintArea::SetBitmap](#setbitmap)|그림 영역에 대 한 비트맵 이미지를 설정합니다.|  
|[CMFCImagePaintArea::SetColor](#setcolor)|현재 그리기 색을 설정합니다.|  
|[CMFCImagePaintArea::SetMode](#setmode)|현재 그리기 모드를 설정합니다.|  
  
### <a name="remarks"></a>설명  
 이 클래스는 사용자 코드에서 직접 사용할 수 없습니다.  
  
 이 클래스를 사용 하 여 이미지 편집기 대화 상자에서 그림 영역을 표시 하는 프레임 워크입니다. 이미지 편집기 대화 상자에 대 한 자세한 내용은 참조 [CMFCImageEditorDialog 클래스](../../mfc/reference/cmfcimageeditordialog-class.md)합니다.  
  
## <a name="example"></a>예제  
 개체를 생성 하는 방법은 다음 예제는 `CMFCImagePaintArea` 클래스를 현재 현재 그리기 모드를 설정 하 고 그림 영역에 대 한 비트맵 이미지 설정 그리기 색을 설정 합니다.  
  
 [!code-cpp[NVC_MFC_RibbonApp #&37;](../../mfc/reference/codesnippet/cpp/cmfcimagepaintarea-class_1.cpp)]  
  
## <a name="inheritance-hierarchy"></a>상속 계층  
 [CObject](../../mfc/reference/cobject-class.md)  
  
 [CCmdTarget](../../mfc/reference/ccmdtarget-class.md)  
  
 [CWnd](../../mfc/reference/cwnd-class.md)  
  
 [CButton](../../mfc/reference/cbutton-class.md)  
  
 [CMFCImagePaintArea](../../mfc/reference/cmfcimagepaintarea-class.md)  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** afximagepaintarea.h  
  
##  <a name="cmfcimagepaintarea"></a>CMFCImagePaintArea::CMFCImagePaintArea  
 `CMFCImagePaintArea` 개체를 생성합니다.  
  
```  
CMFCImagePaintArea(CMFCImageEditorDialog* pParentDlg);
```  
  
### <a name="parameters"></a>매개 변수  
  
|||  
|-|-|  
|매개 변수|설명|  
|[in] `pParentDlg`|이미지 편집기의 부모가 되는 대화 상자에 대 한 포인터입니다.|  
  
##  <a name="getmode"></a>CMFCImagePaintArea::GetMode  
 현재 그리기 모드를 검색합니다.  
  
```  
IMAGE_EDIT_MODE GetMode() const;  
```  
  
### <a name="return-value"></a>반환 값  
 [IMAGE_EDIT_MODE](cmfcimagepaintarea-image-edit-mode-enumeration.md) 현재 그리기 모드를 지정 하는 값입니다.  
  
##  <a name="setbitmap"></a>CMFCImagePaintArea::SetBitmap  
 그림 영역에 대 한 비트맵 이미지를 설정합니다.  
  
```  
void SetBitmap(CBitmap* pBitmap);
```  
  
### <a name="parameters"></a>매개 변수  
  
|||  
|-|-|  
|매개 변수|설명|  
|[in] `pBitmap`|표시할 새 비트맵 이미지를 지정 합니다.|  
  
### <a name="remarks"></a>주의  
 경우 `pBitmap` 는 `NULL`,이 메서드는 수정할 수 있는 그리기 영역의 크기를&0;으로 설정 합니다. 그렇지 않으면 제공 된 비트맵 이미지의 크기를 수정할 수 있는 그리기 영역의 크기를 설정합니다.  
  
##  <a name="setcolor"></a>CMFCImagePaintArea::SetColor  
 현재 그리기 색을 설정합니다.  
  
```  
void SetColor(COLORREF color);
```  
  
### <a name="parameters"></a>매개 변수  
  
|||  
|-|-|  
|매개 변수|설명|  
|[in] `color`|새 드로잉 색입니다.|  
  
### <a name="remarks"></a>주의  
 이미지 편집기 팔레트 막대에서 색을 선택 하거나 때 색 선택, 프레임 워크는 현재 그리기 색을 업데이트 하려면이 메서드를 호출 합니다. 초기 그리기 색은 검정 (한 `COLORREF` 값 0).  
  
 그리기 색을 제외 하 고 모든 그리기 모드에 대 한 이미지 편집기 대화 상자에서 사용 됩니다 `IMAGE_EDIT_MODE_COLOR`합니다. 그리기 모드에 대 한 자세한 내용은 참조 [cmfcimagepaintarea:: Image_edit_mode 열거형](cmfcimagepaintarea-image-edit-mode-enumeration.md)합니다.  
  
##  <a name="setmode"></a>CMFCImagePaintArea::SetMode  
 현재 그리기 모드를 설정합니다.  
  
```  
void SetMode(IMAGE_EDIT_MODE mode);
```  
  
### <a name="parameters"></a>매개 변수  
  
|||  
|-|-|  
|매개 변수|설명|  
|[in] `mode`|[IMAGE_EDIT_MODE](cmfcimagepaintarea-image-edit-mode-enumeration.md) 현재 그리기 모드를 지정 하는 값입니다.|  
  
## <a name="see-also"></a>참고 항목  
 [계층 구조 차트](../../mfc/hierarchy-chart.md)   
 [클래스](../../mfc/reference/mfc-classes.md)   
 [CMFCImageEditorDialog 클래스](../../mfc/reference/cmfcimageeditordialog-class.md)
