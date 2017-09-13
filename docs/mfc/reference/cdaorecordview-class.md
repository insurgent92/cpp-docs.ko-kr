---
title: "CDaoRecordView 클래스 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- CDaoRecordView
- AFXDAO/CDaoRecordView
- AFXDAO/CDaoRecordView::CDaoRecordView
- AFXDAO/CDaoRecordView::IsOnFirstRecord
- AFXDAO/CDaoRecordView::IsOnLastRecord
- AFXDAO/CDaoRecordView::OnGetRecordset
- AFXDAO/CDaoRecordView::OnMove
dev_langs:
- C++
helpviewer_keywords:
- CDaoRecordView class
- data-bound controls [C++], DAO controls
- data binding [C++], DAO views
- bound controls [C++], displaying database data
- application wizards [C++], creating record views
- controls [MFC], data binding
ms.assetid: 5aa7d0e2-bd05-413e-b216-80c404ce18ac
caps.latest.revision: 23
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
ms.openlocfilehash: 11aa318e84e89835ceb710725590f3c3e6387fcd
ms.contentlocale: ko-kr
ms.lasthandoff: 02/24/2017

---
# <a name="cdaorecordview-class"></a>CDaoRecordView 클래스
컨트롤에 데이터베이스 레코드를 표시하는 뷰입니다.  
  
## <a name="syntax"></a>구문  
  
```  
class AFX_NOVTABLE CDaoRecordView : public CFormView  
```  
  
## <a name="members"></a>멤버  
  
### <a name="protected-constructors"></a>Protected 생성자  
  
|이름|설명|  
|----------|-----------------|  
|[CDaoRecordView::CDaoRecordView](#cdaorecordview)|`CDaoRecordView` 개체를 생성합니다.|  
  
### <a name="public-methods"></a>Public 메서드  
  
|이름|설명|  
|----------|-----------------|  
|[CDaoRecordView::IsOnFirstRecord](#isonfirstrecord)|현재 레코드 관련된 레코드 집합에서 첫 번째 레코드인 경우&0;이 아닌 값을 반환 합니다.|  
|[CDaoRecordView::IsOnLastRecord](#isonlastrecord)|현재 레코드 관련된 레코드 집합의 마지막 레코드 이면&0;이 아닌 값을 반환 합니다.|  
|[CDaoRecordView::OnGetRecordset](#ongetrecordset)|포인터에서 파생 된 클래스의 개체를 반환 `CDaoRecordset`합니다. 클래스 마법사는이 함수를 재정의 하 고 필요한 경우 레코드 집합을 만듭니다.|  
|[CDaoRecordView::OnMove](#onmove)|현재 레코드가 변경 된 경우 데이터 원본에서 업데이트 한 다음 지정 된 레코드로 이동 (다음, 이전, 첫 번째 또는 마지막).|  
  
## <a name="remarks"></a>주의  
 뷰는에 직접 연결 하는 폼 보기는 `CDaoRecordset` 개체입니다. 뷰는 대화 상자 템플릿 리소스에서 만들어지고의 필드를 표시 하는 `CDaoRecordset` 대화 상자 템플릿의 컨트롤에 개체입니다. `CDaoRecordView` 개체 대화 상자 데이터 교환 (DDX) 및 DAO 레코드 필드 교환 (DFX) 사용 하 여 폼에 컨트롤 및 레코드 집합의 필드 간의 데이터 이동을 자동화 합니다. `CDaoRecordView`또한 이동에 대 한 기본 구현을 제공 하 고 첫 다음, 이전 또는 마지막 레코드와 보기에서 현재 레코드를 업데이트 하기 위한 인터페이스입니다.  
  
> [!NOTE]
>  DAO 데이터베이스 클래스에 연결 ODBC (Open Database)을 기반으로 하는 MFC 데이터베이스 클래스와 구별 됩니다. 모든 DAO 데이터베이스 클래스 이름이 "CDao" 접두사가 있습니다. 여전히 DAO 클래스; ODBC 데이터 원본에 액세스할 수 있습니다. DAO 클래스 Microsoft Jet 데이터베이스 엔진을 사용 하기 때문에 일반적으로 뛰어난 기능을 제공 합니다.  
  
 레코드 보기를 만드는 가장 일반적인 방법은 응용 프로그램 마법사는 것입니다. 응용 프로그램 마법사는 레코드 뷰 클래스와 스 켈 레 톤 시작 응용 프로그램의 일부로 해당 관련된 레코드 집합 클래스를 만듭니다.  
  
 단일 폼 하기만 하는 응용 프로그램 마법사 방법은 쉽습니다. 클래스 마법사를 사용 하면 레코드 뷰를 사용 하 여 개발 프로세스의 뒷부분에 나오는 하도록 결정할 수 있습니다. 레코드 뷰 클래스 만들지 않으면 응용 프로그램 마법사를 사용 하는 경우 클래스 마법사와 나중에 만들 수 있습니다. 클래스 마법사를 사용 하 여 레코드 뷰 및 레코드 집합을 별도로 만들를 다음에 연결 되므로 가장 융통성이 높은 방법은 레코드 집합 클래스 명명에 더 많은 제어 하 고 있습니다. H /입니다. CPP 파일입니다. 또한이 방법은 동일한 레코드 집합 클래스에 대해 여러 레코드 뷰를 포함할 수 있습니다.  
  
 레코드 뷰에 레코드 간을 이동 하려면 최종 사용자가 쉽게 응용 프로그램 마법사 메뉴 (및 필요에 따라 도구 모음)을 만듭니다 이동에 대 한 리소스는 첫 다음, 이전 또는 마지막 레코드입니다. 클래스 마법사도 레코드 뷰 클래스를 만들면 이러한 리소스를 만들 사용자가 직접 메뉴와 비트맵 편집기 해야 합니다.  
  
 레코드 간을 이동 하기 위한 기본 구현에 대 한 정보를 참조 하십시오. `IsOnFirstRecord` 및 `IsOnLastRecord` 및 문서 [레코드 뷰를 사용 하 여](../../data/using-a-record-view-mfc-data-access.md), 둘 다에 적용 되는 `CRecordView` 및 `CDaoRecordView`합니다.  
  
 `CDaoRecordView`레코드 뷰 사용자 인터페이스를 업데이트할 수 있도록 레코드 집합에서 사용자의 위치는 추적 합니다. 사용자가 레코드 집합의 한쪽 끝을 이동 하는 경우 레코드 뷰 사용자 인터페이스 개체를 비활성화 하는-메뉴 항목이 나 도구 모음 단추와 같은-이동 하기 위한 같은 방향으로 추가 합니다.  
  
 선언 및 레코드 뷰 및 레코드 집합 클래스를 사용 하는 방법에 대 한 자세한 내용은 문서에 "디자인 및 만들기 레코드" 뷰 참조 [레코드 뷰](../../data/record-views-mfc-data-access.md)합니다. 레코드 작업을 보는 방법 및 사용 하는 방법에 대 한 자세한 내용은 문서를 참조 하십시오. [레코드 뷰를 사용 하 여](../../data/using-a-record-view-mfc-data-access.md)합니다. 위에서 언급 한 모든 문서에 모두 적용 `CRecordView` 및 `CDaoRecordView`합니다.  
  
## <a name="inheritance-hierarchy"></a>상속 계층  
 [CObject](../../mfc/reference/cobject-class.md)  
  
 [CCmdTarget](../../mfc/reference/ccmdtarget-class.md)  
  
 [CWnd](../../mfc/reference/cwnd-class.md)  
  
 [CView](../../mfc/reference/cview-class.md)  
  
 [CScrollView](../../mfc/reference/cscrollview-class.md)  
  
 [CFormView](../../mfc/reference/cformview-class.md)  
  
 `CDaoRecordView`  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** afxdao.h  
  
##  <a name="cdaorecordview"></a>CDaoRecordView::CDaoRecordView  
 파생 된 형식의 개체를 만들 때 `CDaoRecordView`, 두 가지 형식의 뷰 개체를 초기화 하 고 보기의 기반이 되는 대화 상자 리소스를 식별 하는 생성자를 호출 합니다.  
  
```  
explicit CDaoRecordView(LPCTSTR lpszTemplateName);  
explicit CDaoRecordView(UINT nIDTemplate);
```  
  
### <a name="parameters"></a>매개 변수  
 `lpszTemplateName`  
 대화 상자 템플릿 리소스의 이름에 해당 하는 null로 끝나는 문자열을 포함 합니다.  
  
 `nIDTemplate`  
 대화 상자 템플릿 리소스의 ID 번호를 포함합니다.  
  
### <a name="remarks"></a>주의  
 (생성자에는 문자열을 인수로 전달) 이름 또는 ID (부호 없는 정수를 인수로 전달)에 하거나 리소스를 식별할 수 있습니다. 리소스 ID는 것이 좋습니다.  
  
> [!NOTE]
>  파생된 클래스의 자체 생성자를 제공 해야 합니다. 파생된 클래스의 생성자에서 생성자를 호출 `CDaoRecordView::CDaoRecordView` 리소스 이름 또는 ID를 인수로 사용 합니다.  
  
 **CDaoRecordView::OnInitialUpdate** 호출 `CWnd::UpdateData`를 호출 하 `CWnd::DoDataExchange`합니다. 이 초기 호출으로 `DoDataExchange` 연결 `CDaoRecordView` (간접적으로) 제어 `CDaoRecordset` 필드 classwizard 함께 사용 하 여 만든 데이터 멤버입니다. 기본 클래스를 호출 하 고 나면 될 때까지 이러한 데이터 멤버를 사용할 수 없습니다 **CFormView::OnInitialUpdate** 멤버 함수입니다.  
  
> [!NOTE]
>  클래스 마법사를 사용 하는 경우 마법사에서 정의 된 `enum` 값 `CDaoRecordView::IDD` 클래스 선언 및 생성자에 대 한 목록 멤버 초기화에 사용 합니다.  
  
 [!code-cpp[NVC_MFCDatabase #&35;](../../mfc/codesnippet/cpp/cdaorecordview-class_1.cpp)]  
  
##  <a name="isonfirstrecord"></a>CDaoRecordView::IsOnFirstRecord  
 현재 레코드가이 레코드 보기와 관련 된 레코드 집합 개체의 첫 번째 레코드 인지 확인 하기 위해이 함수를 호출 합니다.  
  
```  
BOOL IsOnFirstRecord();
```  
  
### <a name="return-value"></a>반환 값  
 현재 레코드는 레코드 집합;의 첫 번째 레코드 0이 아닌 그렇지 않으면 0입니다.  
  
### <a name="remarks"></a>주의  
 이 함수는 기본값의 자체 구현을 classwizard 함께 사용 하 여 작성 된 명령 업데이트 처리기를 작성할 때 유용 합니다.  
  
 사용자가 첫 번째 레코드를 이동 하면 모든 사용자 인터페이스 개체 (예: 메뉴 항목, 도구 모음 단추) 프레임 워크 비활성화 해야는 첫 번째 또는 이전 레코드를 이동 하기 위한.  
  
##  <a name="isonlastrecord"></a>CDaoRecordView::IsOnLastRecord  
 현재 레코드가이 레코드 보기와 관련 된 레코드 집합 개체에서 마지막 레코드 인지 확인 하기 위해이 함수를 호출 합니다.  
  
```  
BOOL IsOnLastRecord();
```  
  
### <a name="return-value"></a>반환 값  
 현재 레코드; 레코드 집합의 마지막 레코드 하면 0이 아니고 그렇지 않으면 0입니다.  
  
### <a name="remarks"></a>주의  
 이 함수는 고유한 구현을 기본 클래스 마법사가 레코드 간을 이동 하기 위한 사용자 인터페이스를 지원 하기 위해 작성 하는 명령 업데이트 처리기를 작성할 때 유용 합니다.  
  
> [!CAUTION]
>  이 함수의 결과 신뢰할 수 있는 제외 하 고 보기를 전달 하는 사용자가 이동 될 때까지 레코드 집합의 끝을 검색할 수 수 있습니다. 사용자는 다음 또는 마지막 레코드로 이동 하는 것에 대 한 모든 사용자 인터페이스 개체를 사용 하지 않도록 설정 해야 하는 레코드 뷰 알 수 전에 마지막 레코드 보다 이동 해야 할 수 있습니다. 사용자 마지막 레코드를 지나서 이동 하 고 다시 마지막 레코드로 이동 하는 경우 (또는 앞) 레코드 뷰 레코드 집합에서 사용자의 위치를 추적할 수 및 사용자 인터페이스 개체를 올바르게 사용 하지 않도록 설정 합니다.  
  
##  <a name="ongetrecordset"></a>CDaoRecordView::OnGetRecordset  
 에 대 한 포인터를 반환 합니다.는 `CDaoRecordset`-레코드 보기와 연결 된 개체를 파생 합니다.  
  
```  
virtual CDaoRecordset* OnGetRecordset() = 0;  
```  
  
### <a name="return-value"></a>반환 값  
 에 대 한 포인터는 `CDaoRecordset`-개체가 성공적으로 생성 하 고 그렇지 않으면 파생 된 개체는 **NULL** 포인터입니다.  
  
### <a name="remarks"></a>주의  
 생성 또는 recordset 개체를 가져오고,에 대 한 포인터를 반환 하려면이 멤버 함수를 재정의 해야 합니다. 클래스 마법사와 레코드 뷰 클래스를 선언 하는 경우 마법사는 기본 재정의를 작성 합니다. 클래스 마법사의 기본 구현은 있을 경우 레코드 뷰에 저장 된 레코드 포인터를 반환 합니다. ClassWizard 및 호출을 사용 하 여 지정한 형식의 레코드 집합 개체를 생성 그렇지 않은 경우 해당 **열고** 멤버 함수는 테이블을 열거나 쿼리를 실행 하 고 다음 개체에 대 한 포인터를 반환 합니다.  
  
 자세한 내용 및 예제에 대 한 문서를 참조 [레코드 뷰: 레코드 뷰를 사용 하 여](../../data/using-a-record-view-mfc-data-access.md)합니다.  
  
##  <a name="onmove"></a>CDaoRecordView::OnMove  
 레코드 집합의 다른 레코드를 이동 하 고 레코드 뷰 컨트롤에서 해당 필드를 표시 하려면이 멤버 함수를 호출 합니다.  
  
```  
virtual BOOL OnMove(UINT nIDMoveCommand);
```  
  
### <a name="parameters"></a>매개 변수  
 `nIDMoveCommand`  
 다음 표준 명령 ID 값 중 하나입니다.  
  
- `ID_RECORD_FIRST`레코드 집합의 첫 번째 레코드를 이동 합니다.  
  
- `ID_RECORD_LAST`레코드는 레코드 집합에서 마지막으로 이동 합니다.  
  
- `ID_RECORD_NEXT`레코드 집합의 다음 레코드로 이동 합니다.  
  
- `ID_RECORD_PREV`레코드 집합의 이전 레코드로 이동 합니다.  
  
### <a name="return-value"></a>반환 값  
 이동에 성공 하면 0이 아닌 그렇지 않으면 0이 고 이동 요청은 거부 되었습니다.  
  
### <a name="remarks"></a>주의  
 적절 한 이동 멤버 함수를 호출 하는 기본 구현에서 `CDaoRecordset` 레코드 보기와 연결 된 개체입니다.  
  
 기본적으로 `OnMove` 사용자 레코드 보기에서 변경 된 경우 데이터 소스에서 현재 레코드를 업데이트 합니다.  
  
 응용 프로그램 마법사는 첫 번째 레코드, 마지막 레코드, 다음 레코드 및 이전 레코드 메뉴 항목과 함께 메뉴 리소스를 만듭니다. 초기 도구 모음 옵션을 선택 하는 경우 응용 프로그램 마법사가이 명령에 해당 하는 단추가 포함 된 도구 모음을 만듭니다.  
  
 레코드 집합의 마지막 레코드를 지난 이동 하는 경우 레코드 뷰 계속 마지막 레코드를 표시 합니다. 첫 번째 레코드를 지 나 뒤로 이동 하는 경우 첫 번째 레코드를 표시 하는 레코드 뷰 계속 합니다.  
  
> [!CAUTION]
>  호출 `OnMove` 레코드 집합에 레코드가 없는 경우 예외를 throw 합니다. 적절 한 사용자 인터페이스 업데이트 처리기 함수를 호출 합니다.- **OnUpdateRecordFirst**, **OnUpdateRecordLast**, **OnUpdateRecordNext**, 또는 **OnUpdateRecordPrev** -해당 하기 전에 레코드 집합에 레코드가 있는지 여부를 결정 하는 작업을 이동 합니다.  
  
## <a name="see-also"></a>참고 항목  
 [CFormView 클래스](../../mfc/reference/cformview-class.md)   
 [계층 구조 차트](../../mfc/hierarchy-chart.md)   
 [CDaoRecordset 클래스](../../mfc/reference/cdaorecordset-class.md)   
 [CDaoTableDef 클래스](../../mfc/reference/cdaotabledef-class.md)   
 [CDaoQueryDef 클래스](../../mfc/reference/cdaoquerydef-class.md)   
 [CDaoDatabase 클래스](../../mfc/reference/cdaodatabase-class.md)   
 [CDaoWorkspace 클래스](../../mfc/reference/cdaoworkspace-class.md)   
 [CFormView 클래스](../../mfc/reference/cformview-class.md)
