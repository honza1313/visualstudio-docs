---
title: "IDiaEnumDebugStreamData::Item"
ms.custom: na
ms.date: 10/03/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 761e61a5-44a6-4d5d-a98e-c2e9b89d2343
caps.latest.revision: 7
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
---
# IDiaEnumDebugStreamData::Item
Retrieves the specified record.  
  
## Syntax  
  
```cpp#  
HRESULT Item (   
   DWORD  index,  
   DWORD  cbData,  
   DWORD* pcbData,  
   BYTE   data[]  
);  
```  
  
#### Parameters  
 index  
 [in] Index of the record to be retrieved. The index is in the range 0 to `count`-1, where `count` is returned by [IDiaEnumDebugStreamData::get_Count](../VS_debugger/IDiaEnumDebugStreamData--get_Count.md).  
  
 cbData  
 [in] Size of the data buffer, in bytes.  
  
 pcbData  
 [out] Returns the number of bytes returned. If `data` is `NULL`, then `pcbData` contains the total number of bytes of data available in the specified record.  
  
 data[]  
 [out] A buffer that is filled in with the debug stream record data.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code. Returns `E_INVALIDARG` for invalid parameters and if the `index` parameter is out of bounds.  
  
## See Also  
 [IDiaEnumDebugStreamData](../VS_debugger/IDiaEnumDebugStreamData.md)   
 [IDiaEnumDebugStreamData::Next](../VS_debugger/IDiaEnumDebugStreamData--Next.md)   
 [IDiaEnumDebugStreams::Item](../VS_debugger/IDiaEnumDebugStreams--Item.md)   
 [IDiaEnumDebugStreamData::get_Count](../VS_debugger/IDiaEnumDebugStreamData--get_Count.md)   
 [IDiaEnumDebugStreamData::Skip](../VS_debugger/IDiaEnumDebugStreamData--Skip.md)