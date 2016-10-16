---
title: "MESSAGETYPE"
ms.custom: na
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "MESSAGETYPE"
helpviewer_keywords: 
  - "MESSAGETYPE enumeration"
ms.assetid: 800cc77d-3c27-4763-a9df-552a9384bd49
caps.latest.revision: 11
ms.author: "gregvanl"
manager: "ghogen"
translation.priority.mt: 
  - "cs-cz"
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "pl-pl"
  - "pt-br"
  - "ru-ru"
  - "tr-tr"
  - "zh-cn"
  - "zh-tw"
---
# MESSAGETYPE
Specifies the message type and reason.  
  
## Syntax  
  
```cpp#  
enum enum_MESSAGETYPE {   
   MT_OUTPUTSTRING      = 0x0000001,  
   MT_MESSAGEBOX        = 0x00000002,  
   MT_TYPE_MASK         = 0x000000FF,  
   MT_REASON_EXCEPTION  = 0x00000100,  
   MT_REASON_TRACEPOINT = 0x00000200,  
   MT_REASON_MASK       = 0x0000FF00  
};  
typedef DWORD MESSAGETYPE;  
```  
  
```c#  
public enum enum_MESSAGETYPE {   
   MT_OUTPUTSTRING      = 0x0000001,  
   MT_MESSAGEBOX        = 0x00000002,  
   MT_TYPE_MASK         = 0x000000FF,  
   MT_REASON_EXCEPTION  = 0x00000100,  
   MT_REASON_TRACEPOINT = 0x00000200,  
   MT_REASON_MASK       = 0x0000FF00  
};  
```  
  
## Members  
 MT_OUTPUTSTRING  
 Indicates that the message should be sent to the output window. This is mutually exclusive from `MT_MESSAGEBOX`.  
  
 MT_MESSAGEBOX  
 Indicates that the message should be shown in a message box. This is mutually exclusive from `MT_OUTPUTSTRING`.  
  
 MT_TYPE_MASK  
 A mask value to isolate the destination for the message.  
  
 MT_REASON_EXCEPTION  
 Indicates that a message box is being shown as a result of an exception. This is mutually exclusive from `MT_REASON_TRACEPOINT`.  
  
 MT_REASON_TRACEPOINT  
 Indicates that a message box is being shown as a result of hitting a tracepoint. This is mutually exclusive to `MT_REASON_EXCEPTION`.  
  
 MT_REASON_MASK  
 A mask value to isolate the reason for the message being shown.  
  
## Remarks  
 These values are returned from the [GetMessage](../extensibility/idebugmessageevent2--getmessage.md) and [GetErrorMessage](../extensibility/idebugerrorevent2--geterrormessage.md) methods.  
  
 One of the reason values can be combined with one of the output destination values using a bitwise `OR`.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Enumerations](../extensibility/enumerations--visual-studio-debugging-.md)   
 [GetMessage](../extensibility/idebugmessageevent2--getmessage.md)   
 [GetErrorMessage](../extensibility/idebugerrorevent2--geterrormessage.md)