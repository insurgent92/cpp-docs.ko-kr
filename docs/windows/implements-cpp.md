---
title: "implements (C++) | Microsoft Docs"
ms.custom: ""
ms.date: "12/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "language-reference"
f1_keywords: 
  - "vc-attr.implements"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "implements attribute"
ms.assetid: 9cf0858b-cb7d-4d3c-81a6-97d87ed00d25
caps.latest.revision: 14
caps.handback.revision: 14
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
---
# implements (C++)
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

IDL coclass의 구성원으로 강제 하는 디스패치 인터페이스를 지정 합니다.  
  
## 구문  
  
```  
  
      [ implements(   
   interfaces={interfaces},  
   dispinterfaces={dispinterfaces}  
)]  
```  
  
#### 매개 변수  
 **인터페이스**  
 IDL coclass의 구성원이 되는 인터페이스 목록을 쉼표로 구분 하는 방법  단일 인터페이스를 지정 하는 대표 방법입니다  **구현 \(***interface\_name***\)**.  
  
 **dispinterfaces**  
 IDL coclass의 구성원이 dispinterface의 목록을 쉼표로 구분 하는 방법  단일 dispinterface를 지정 하는 대표 방법입니다  **구현 \(dispinterfaces** *dispinterface\_name \=***\)**.  
  
## 설명  
 기본적으로는 COM\-기본 클래스에는 coclass 인터페이스는 IDL coclass에 추가 됩니다.  **구현** IDL coclass 구성원으로 다른 인터페이스를 강제로 수 있습니다.  
  
## 요구 사항  
  
### 컨텍스트 특성  
  
|||  
|-|-|  
|**적용 대상**|**클래스**,`struct`|  
|**반복 가능**|예|  
|**필수 특성**|없음|  
|**잘못 된 특성**|없음|  
  
 자세한 내용은  [컨텍스트 특성](../windows/attribute-contexts.md).  
  
## 예제  
 다음 예제에서는 세 가지 부분으로 구성 되어:.idl 파일 및 해당 관련된.h 파일 및 C\+\+ 파일입니다.  
  
 컴파일러에 사용할 수 있습니다 다음.idl 파일이 있다고 가정 합니다.  
  
```  
// attr_implements.idl  
import "docobj.idl";  
[ version(1.0), uuid(0ed71801-a1b6-3178-af3b-9431fc00185e) ]  
library odod  
{  
   importlib("stdole2.tlb");  
   importlib("olepro32.dll");  
  
   [  
      object,  
      uuid(1AECC9BB-2104-3723-98B8-7CC54722C7DD)  
   ]   
   interface IBar1 {  
      [id(1)] HRESULT bar1();  
   };  
  
   [  
      dual,  
      uuid(1AECCABB-2104-3723-98B8-7CC54722C7DD)  
   ]   
   interface IBar2 {  
      [id(1)] HRESULT bar2();  
   };  
  
   [  
      uuid(1AECC9CC-2104-3723-98B8-7CC54722C7DD)  
   ]   
   dispinterface ISna {  
   properties:  
  
   methods:  
      [id(1)] HRESULT sna();  
   };  
  
   [  
      uuid(159A9BBB-E5F1-33F6-BEF5-6CFAD7A5933F),  
      version(1.0)  
   ]   
   coclass CBar {  
      interface IBar1;  
      interface IBar2;  
      dispinterface ISna;  
   };  
}  
```  
  
## 예제  
 및 다음.h 파일 또한 컴파일러를 사용할 수 있어야 합니다.  
  
```  
// attr_implements.h  
// this ALWAYS GENERATED file contains definitions for the interfaces  
  
/* File created by MIDL compiler version 6.00.0361 */  
/* at Mon Feb 28 16:30:53 2005 */  
/* Compiler settings for attr_implements.idl:  
    Oicf, W1, Zp8, env=Win32 (32b run)  
    protocol : dce , ms_ext, c_ext, robust  
    error checks: allocation ref bounds_check enum stub_data   
    VC __declspec() decoration level:   
         __declspec(uuid()), __declspec(selectany), __declspec(novtable)  
         DECLSPEC_UUID(), MIDL_INTERFACE()  
*/  
//@@MIDL_FILE_HEADING(  )  
  
#pragma warning( disable: 4049 )  /* more than 64k source lines */  
  
/* verify that the <rpcndr.h> version is high enough to compile this file*/  
#ifndef __REQUIRED_RPCNDR_H_VERSION__  
#define __REQUIRED_RPCNDR_H_VERSION__ 475  
#endif  
  
#include "rpc.h"  
#include "rpcndr.h"  
  
#ifndef __RPCNDR_H_VERSION__  
#error this stub requires an updated version of <rpcndr.h>  
#endif // __RPCNDR_H_VERSION__  
  
#ifndef __attr_implements_h__  
#define __attr_implements_h__  
  
#if defined(_MSC_VER) && (_MSC_VER >= 1020)  
#pragma once  
#endif  
  
/* Forward Declarations */   
  
#ifndef __IBar1_FWD_DEFINED__  
#define __IBar1_FWD_DEFINED__  
typedef interface IBar1 IBar1;  
#endif /* __IBar1_FWD_DEFINED__ */  
  
#ifndef __IBar2_FWD_DEFINED__  
#define __IBar2_FWD_DEFINED__  
typedef interface IBar2 IBar2;  
#endif /* __IBar2_FWD_DEFINED__ */  
  
#ifndef __ISna_FWD_DEFINED__  
#define __ISna_FWD_DEFINED__  
typedef interface ISna ISna;  
#endif /* __ISna_FWD_DEFINED__ */  
  
#ifndef __CBar_FWD_DEFINED__  
#define __CBar_FWD_DEFINED__  
  
#ifdef __cplusplus  
typedef class CBar CBar;  
#else  
typedef struct CBar CBar;  
#endif /* __cplusplus */  
  
#endif /* __CBar_FWD_DEFINED__ */  
  
/* header files for imported files */  
#include "docobj.h"  
  
#ifdef __cplusplus  
extern "C"{  
#endif   
  
void * __RPC_USER MIDL_user_allocate(size_t);  
void __RPC_USER MIDL_user_free( void * );   
  
#ifndef __odod_LIBRARY_DEFINED__  
#define __odod_LIBRARY_DEFINED__  
  
/* library odod */  
/* [uuid][version] */   
  
EXTERN_C const IID LIBID_odod;  
  
#ifndef __IBar1_INTERFACE_DEFINED__  
#define __IBar1_INTERFACE_DEFINED__  
  
/* interface IBar1 */  
/* [uuid][object] */   
  
EXTERN_C const IID IID_IBar1;  
  
#if defined(__cplusplus) && !defined(CINTERFACE)  
  
    MIDL_INTERFACE("1AECC9BB-2104-3723-98B8-7CC54722C7DD")  
    IBar1  
    {  
    public:  
        BEGIN_INTERFACE  
        virtual /* [id] */ HRESULT STDMETHODCALLTYPE bar1( void) = 0;  
  
        END_INTERFACE  
    };  
  
#else /* C style interface */  
  
    typedef struct IBar1Vtbl  
    {  
        BEGIN_INTERFACE  
  
        /* [id] */ HRESULT ( STDMETHODCALLTYPE *bar1 )(   
            IBar1 * This);  
  
        END_INTERFACE  
    } IBar1Vtbl;  
  
    interface IBar1  
    {  
        CONST_VTBL struct IBar1Vtbl *lpVtbl;  
    };  
  
#ifdef COBJMACROS  
  
#define IBar1_bar1(This)\  
    (This)->lpVtbl -> bar1(This)  
  
#endif /* COBJMACROS */  
  
#endif /* C style interface */  
  
/* [id] */ HRESULT STDMETHODCALLTYPE IBar1_bar1_Proxy(   
    IBar1 * This);  
  
void __RPC_STUB IBar1_bar1_Stub(  
    IRpcStubBuffer *This,  
    IRpcChannelBuffer *_pRpcChannelBuffer,  
    PRPC_MESSAGE _pRpcMessage,  
    DWORD *_pdwStubPhase);  
  
#endif /* __IBar1_INTERFACE_DEFINED__ */  
  
#ifndef __IBar2_INTERFACE_DEFINED__  
#define __IBar2_INTERFACE_DEFINED__  
  
/* interface IBar2 */  
/* [auto_handle][uuid][dual] */   
  
EXTERN_C const IID IID_IBar2;  
  
#if defined(__cplusplus) && !defined(CINTERFACE)  
  
    MIDL_INTERFACE("1AECCABB-2104-3723-98B8-7CC54722C7DD")  
    IBar2  
    {  
    public:  
        BEGIN_INTERFACE  
        virtual /* [id] */ HRESULT STDMETHODCALLTYPE bar2( void) = 0;  
  
        END_INTERFACE  
    };  
  
#else /* C style interface */  
  
    typedef struct IBar2Vtbl  
    {  
        BEGIN_INTERFACE  
  
        /* [id] */ HRESULT ( STDMETHODCALLTYPE *bar2 )(   
            IBar2 * This);  
  
        END_INTERFACE  
    } IBar2Vtbl;  
  
    interface IBar2  
    {  
        CONST_VTBL struct IBar2Vtbl *lpVtbl;  
    };  
  
#ifdef COBJMACROS  
  
#define IBar2_bar2(This)\  
    (This)->lpVtbl -> bar2(This)  
  
#endif /* COBJMACROS */  
  
#endif /* C style interface */  
  
/* [id] */ HRESULT STDMETHODCALLTYPE IBar2_bar2_Proxy(   
    IBar2 * This);  
  
void __RPC_STUB IBar2_bar2_Stub(  
    IRpcStubBuffer *This,  
    IRpcChannelBuffer *_pRpcChannelBuffer,  
    PRPC_MESSAGE _pRpcMessage,  
    DWORD *_pdwStubPhase);  
  
#endif /* __IBar2_INTERFACE_DEFINED__ */  
  
#ifndef __ISna_DISPINTERFACE_DEFINED__  
#define __ISna_DISPINTERFACE_DEFINED__  
  
/* dispinterface ISna */  
/* [uuid] */   
  
EXTERN_C const IID DIID_ISna;  
  
#if defined(__cplusplus) && !defined(CINTERFACE)  
  
    MIDL_INTERFACE("1AECC9CC-2104-3723-98B8-7CC54722C7DD")  
    ISna : public IDispatch  
    {  
    };  
  
#else /* C style interface */  
  
    typedef struct ISnaVtbl  
    {  
        BEGIN_INTERFACE  
  
        HRESULT ( STDMETHODCALLTYPE *QueryInterface )(   
            ISna * This,  
            /* [in] */ REFIID riid,  
            /* [iid_is][out] */ void **ppvObject);  
  
        ULONG ( STDMETHODCALLTYPE *AddRef )(   
            ISna * This);  
  
        ULONG ( STDMETHODCALLTYPE *Release )(   
            ISna * This);  
  
        HRESULT ( STDMETHODCALLTYPE *GetTypeInfoCount )(   
            ISna * This,  
            /* [out] */ UINT *pctinfo);  
  
        HRESULT ( STDMETHODCALLTYPE *GetTypeInfo )(   
            ISna * This,  
            /* [in] */ UINT iTInfo,  
            /* [in] */ LCID lcid,  
            /* [out] */ ITypeInfo **ppTInfo);  
  
        HRESULT ( STDMETHODCALLTYPE *GetIDsOfNames )(   
            ISna * This,  
            /* [in] */ REFIID riid,  
            /* [size_is][in] */ LPOLESTR *rgszNames,  
            /* [in] */ UINT cNames,  
            /* [in] */ LCID lcid,  
            /* [size_is][out] */ DISPID *rgDispId);  
  
        /* [local] */ HRESULT ( STDMETHODCALLTYPE *Invoke )(   
            ISna * This,  
            /* [in] */ DISPID dispIdMember,  
            /* [in] */ REFIID riid,  
            /* [in] */ LCID lcid,  
            /* [in] */ WORD wFlags,  
            /* [out][in] */ DISPPARAMS *pDispParams,  
            /* [out] */ VARIANT *pVarResult,  
            /* [out] */ EXCEPINFO *pExcepInfo,  
            /* [out] */ UINT *puArgErr);  
  
        END_INTERFACE  
    } ISnaVtbl;  
  
    interface ISna  
    {  
        CONST_VTBL struct ISnaVtbl *lpVtbl;  
    };  
  
#ifdef COBJMACROS  
  
#define ISna_QueryInterface(This,riid,ppvObject)\  
    (This)->lpVtbl -> QueryInterface(This,riid,ppvObject)  
  
#define ISna_AddRef(This)\  
    (This)->lpVtbl -> AddRef(This)  
  
#define ISna_Release(This)\  
    (This)->lpVtbl -> Release(This)  
  
#define ISna_GetTypeInfoCount(This,pctinfo)\  
    (This)->lpVtbl -> GetTypeInfoCount(This,pctinfo)  
  
#define ISna_GetTypeInfo(This,iTInfo,lcid,ppTInfo)\  
    (This)->lpVtbl -> GetTypeInfo(This,iTInfo,lcid,ppTInfo)  
  
#define ISna_GetIDsOfNames(This,riid,rgszNames,cNames,lcid,rgDispId)\  
    (This)->lpVtbl -> GetIDsOfNames(This,riid,rgszNames,cNames,lcid,rgDispId)  
  
#define ISna_Invoke(This,dispIdMember,riid,lcid,wFlags,pDispParams,pVarResult,pExcepInfo,puArgErr)\  
    (This)->lpVtbl -> Invoke(This,dispIdMember,riid,lcid,wFlags,pDispParams,pVarResult,pExcepInfo,puArgErr)  
  
#endif /* COBJMACROS */  
  
#endif /* C style interface */  
  
#endif /* __ISna_DISPINTERFACE_DEFINED__ */  
  
EXTERN_C const CLSID CLSID_CBar;  
  
#ifdef __cplusplus  
  
class DECLSPEC_UUID("159A9BBB-E5F1-33F6-BEF5-6CFAD7A5933F")  
CBar;  
#endif  
#endif /* __odod_LIBRARY_DEFINED__ */  
  
/* Additional Prototypes for ALL interfaces */  
  
/* end of Additional Prototypes */  
  
#ifdef __cplusplus  
}  
#endif  
#endif  
```  
  
## 예제  
 다음 프로그램에서 구현 하지 않고 IBar1, IBar2, 및 Isna는에서 생성 된 IDL coclass에 수 없습니다.  
  
```  
// attr_implements.cpp  
// compile with: /LD /link /idlout:out.idl  
#define _ATL_ATTRIBUTES 1  
#include <atlbase.h>  
#include <atlcom.h>  
#include "attr_implements.h"   // IDL generated header that contains a definition of the pseudo-interface IBar and pseudo-dispinterface  ISna  
  
[module(name = "MyLib")];  
  
[dispinterface, uuid("00000000-0000-0000-0000-000000000001")]   
__interface IMyInterface  
{  
   [id(0)] long x;  
   [id(1)] HRESULT func();  
};  
  
[  
   coclass,  
   uuid("00000000-0000-0000-0000-000000000002"),  
   implements(interfaces={IBar1,IBar2}, dispinterfaces=ISna)  
]   
class CMyClass : public IMyInterface,   
   public IBar1,  
      public IDispatchImpl<IBar2, &__uuidof(IBar2)>,   
   public ISna  
{  
   long _x;  
public:  
   long get_x() { return _x; }  
   void put_x(long x0) { _x = x0; }  
   HRESULT func() { return S_OK; }  
   HRESULT __stdcall bar1() { return S_OK; }  
   HRESULT __stdcall bar2() { return S_OK; }  
   HRESULT __stdcall sna() { return S_OK; }  
  
   virtual HRESULT STDMETHODCALLTYPE ISna::Invoke(  
            /* [in] */ DISPID dispIdMember,  
            /* [in] */ REFIID riid,  
            /* [in] */ LCID lcid,  
            /* [in] */ WORD wFlags,  
            /* [out][in] */ DISPPARAMS *pDispParams,  
            /* [out] */ VARIANT *pVarResult,  
            /* [out] */ EXCEPINFO *pExcepInfo,  
            /* [out] */ UINT *puArgErr)   
   {  
      HRESULT hr = S_OK;  
      if (pDispParams == 0) {  
         return DISP_E_BADVARTYPE;  
      }  
      if (pDispParams->cArgs > 0) {  
         return DISP_E_BADPARAMCOUNT;  
      }  
      if (pVarResult != 0) {  
         ::VariantInit(pVarResult);  
      }  
      switch (dispIdMember) {  
      case 1:  
         {  
            if (pDispParams->cArgs != 0) {  
               return DISP_E_BADPARAMCOUNT;  
            }  
            hr = this->sna();  
            break;  
         }  
      default:  
         return DISP_E_MEMBERNOTFOUND;  
      }  
      return hr;  
   }  
   virtual HRESULT STDMETHODCALLTYPE ISna::GetIDsOfNames(  
            /* [in] */ REFIID riid,  
            /* [size_is][in] */ LPOLESTR *rgszNames,  
            /* [in] */ UINT cNames,  
            /* [in] */ LCID lcid,  
            /* [size_is][out] */ DISPID *rgDispId)   
   {  
      static LPOLESTR names[] = { L"sna" };  
      static DISPID dids[] = { 1 };  
      for (unsigned int i = 0; i < cNames; ++i) {  
         int fFoundIt = 0;  
         for (unsigned int j = 0; j < sizeof(names)/sizeof(LPOLESTR); ++j) {  
            if (lstrcmpiW(rgszNames[i], names[j]) == 0) {  
               fFoundIt = 1;  
               rgDispId[i] = dids[j];  
               break;  
            }  
         }  
         if (fFoundIt == 0) {  
            return DISP_E_UNKNOWNNAME;  
         }  
      }  
      return S_OK;  
   }  
   virtual HRESULT STDMETHODCALLTYPE ISna::GetTypeInfoCount(unsigned int*  pctinfo)   
   {  
      if (pctinfo == NULL) {  
         return E_POINTER;  
      }  
      CComPtr<ITypeInfo> spTypeInfo;  
      *pctinfo =   
                  (SUCCEEDED(TypeInfoHelper(__uuidof(ISna), 0, &spTypeInfo))) ? 1 : 0;  
      return S_OK;  
   }  
   virtual HRESULT STDMETHODCALLTYPE ISna::GetTypeInfo(unsigned int iTInfo, LCID lcid, ITypeInfo** ppTInfo)   
   {  
      if (iTInfo != 0) {  
         return DISP_E_BADINDEX;  
      }  
      return TypeInfoHelper(__uuidof(ISna), lcid, ppTInfo);  
   }  
   BEGIN_COM_MAP(CMyClass)  
      COM_INTERFACE_ENTRY(IBar1)  
      COM_INTERFACE_ENTRY(IBar2)  
      COM_INTERFACE_ENTRY(ISna)  
   END_COM_MAP()  
};  
```  
  
## 참고 항목  
 [Compiler Attributes](../windows/compiler-attributes.md)   
 [Class Attributes](../windows/class-attributes.md)   
 [Attributes Samples](http://msdn.microsoft.com/ko-kr/558ebdb2-082f-44dc-b442-d8d33bf7bdb8)