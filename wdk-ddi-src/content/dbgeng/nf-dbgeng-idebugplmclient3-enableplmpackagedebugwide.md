---
UID: NF:dbgeng.IDebugPlmClient3.EnablePlmPackageDebugWide
title: IDebugPlmClient3::EnablePlmPackageDebugWide method
author: windows-driver-content
description: Enables a Process Lifecycle Management (PLM) package debug.
old-location: debugger\idebugplmclient3_enableplmpackagedebugwide.htm
old-project: debugger
ms.assetid: 6373B8BD-264D-4D03-9FE9-F87E45D617EE
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: EnablePlmPackageDebugWide method [Windows Debugging], EnablePlmPackageDebugWide method [Windows Debugging], IDebugPlmClient3 interface, EnablePlmPackageDebugWide,IDebugPlmClient3.EnablePlmPackageDebugWide, IDebugPlmClient3, IDebugPlmClient3 interface [Windows Debugging], EnablePlmPackageDebugWide method, IDebugPlmClient3::EnablePlmPackageDebugWide, dbgeng/IDebugPlmClient3::EnablePlmPackageDebugWide, debugger.idebugplmclient3_enableplmpackagedebugwide
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dbgeng.h
req.include-header: Dbgeng.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dbgeng.h
api_name:
-	IDebugPlmClient3.EnablePlmPackageDebugWide
product: Windows
targetos: Windows
req.typenames: DOT4_ACTIVITY, *PDOT4_ACTIVITY
---

# IDebugPlmClient3::EnablePlmPackageDebugWide method


## -description


Enables a Process Lifecycle Management (PLM) package debug.


## -syntax


````
HRESULT EnablePlmPackageDebugWide(
  [in] ULONG64 Server,
  [in] PCWSTR  PackageFullName
);
````


## -parameters




### -param Server [in]

The server of the package.


### -param PackageFullName [in]

A pointer to the package name.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also

<a href="..\dbgeng\nn-dbgeng-idebugplmclient3.md">IDebugPlmClient3</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [debugger\debugger]:%20IDebugPlmClient3::EnablePlmPackageDebugWide method%20 RELEASE:%20(2/27/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

