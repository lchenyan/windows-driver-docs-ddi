---
UID: NF:dbgeng.IDebugSymbols3.SetScopeFromStoredEvent
title: IDebugSymbols3::SetScopeFromStoredEvent method
author: windows-driver-content
description: The SetScopeFromStoredEvent method sets the current scope to the scope of the stored event.
old-location: debugger\setscopefromstoredevent.htm
old-project: debugger
ms.assetid: 34c50e32-37c8-4e6a-a666-fce8880cb000
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: IDebugSymbols3, IDebugSymbols3 interface [Windows Debugging], SetScopeFromStoredEvent method, IDebugSymbols3::SetScopeFromStoredEvent, IDebugSymbols_710b59d8-620b-479f-bfeb-dd1196cd2dbc.xml, SetScopeFromStoredEvent method [Windows Debugging], SetScopeFromStoredEvent method [Windows Debugging], IDebugSymbols3 interface, SetScopeFromStoredEvent,IDebugSymbols3.SetScopeFromStoredEvent, dbgeng/IDebugSymbols3::SetScopeFromStoredEvent, debugger.setscopefromstoredevent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dbgeng.h
req.include-header: Dbgeng.h
req.target-type: Desktop
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
-	Dbgeng.h
api_name:
-	IDebugSymbols3.SetScopeFromStoredEvent
product: Windows
targetos: Windows
req.typenames: DOT4_ACTIVITY, *PDOT4_ACTIVITY
---

# IDebugSymbols3::SetScopeFromStoredEvent method


## -description


The <b>SetScopeFromStoredEvent</b> method sets the current scope to the scope of the stored event.


## -syntax


````
HRESULT SetScopeFromStoredEvent();
````


## -parameters






## -returns



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
</table>
 

This method may also return error values.  See <a href="https://msdn.microsoft.com/713f3ee2-2f5b-415e-9908-90f5ae428b43">Return Values</a> for more details.




## -remarks



Currently only user-mode<a href="https://msdn.microsoft.com/library/windows/hardware/ff552212">Minidumps</a> can contain a stored event.

The new scope is printed to the debugger console.

For more information about scopes, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff554702">Scopes and Symbol Groups</a>.




## -see-also

<a href="..\dbgeng\nn-dbgeng-idebugsymbols3.md">IDebugSymbols3</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff548431">GetStoredEventInformation</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556774">SetScopeFrameByIndex</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff562945">.ecxr (Display Exception Context Record)</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556773">SetScope</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [debugger\debugger]:%20IDebugSymbols3::SetScopeFromStoredEvent method%20 RELEASE:%20(2/27/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

