---
title: "Compiler Warning (level 1) CS3014"
ms.custom: na
ms.date: 10/01/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6825b42f-1820-4265-b8d8-9b3387d7c130
caps.latest.revision: 12
manager: douge
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
# Compiler Warning (level 1) CS3014
'member' does not need a CLSCompliant attribute because the assembly does not have a CLSCompliant attribute  
  
 In a source code file where compliance with the Common Language Specification (CLS) was not specified, a construct in the file was marked as being CLS compliant. This is not allowed. To resolve this warning, add an assembly level CLS compliant attribute to the file (in the following example, uncomment the line that contains the assembly level attribute). For more information about CLS Compliance, see [Writing CLS-Compliant Code](assetId:///4c705105-69a2-4e5e-b24e-0633bc32c7f3) and [Language Independence and Language-Independent Components](../Topic/Language%20Independence%20and%20Language-Independent%20Components.md).  
  
## Example  
 The following example generates CS3014:  
  
```  
// CS3014.cs  
  
using System;  
  
// [assembly:CLSCompliant(true)]  
public class I  
{  
    [CLSCompliant(true)]   // CS3014  
    public void M()  
    {  
    }  
  
    public static void Main()  
    {  
    }  
}  
```