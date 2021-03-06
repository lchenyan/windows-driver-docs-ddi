---
UID: NF:dbgeng.IDebugControl3.GetNotifyEventHandle
title: IDebugControl3::GetNotifyEventHandle method
author: windows-driver-content
description: The GetNotifyEventHandle method receives the handle of the event that will be signaled after the next exception in a target.
old-location: debugger\getnotifyeventhandle.htm
old-project: debugger
ms.assetid: a949a583-1ee1-4538-9117-4ad1482e8bc8
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: GetNotifyEventHandle method [Windows Debugging], GetNotifyEventHandle method [Windows Debugging], IDebugControl interface, GetNotifyEventHandle method [Windows Debugging], IDebugControl2 interface, GetNotifyEventHandle method [Windows Debugging], IDebugControl3 interface, GetNotifyEventHandle,IDebugControl3.GetNotifyEventHandle, IDebugControl interface [Windows Debugging], GetNotifyEventHandle method, IDebugControl2 interface [Windows Debugging], GetNotifyEventHandle method, IDebugControl2::GetNotifyEventHandle, IDebugControl3, IDebugControl3 interface [Windows Debugging], GetNotifyEventHandle method, IDebugControl3::GetNotifyEventHandle, IDebugControl::GetNotifyEventHandle, IDebugControl_73931ad2-ace6-4d38-ad22-c322f2e3c13c.xml, dbgeng/IDebugControl2::GetNotifyEventHandle, dbgeng/IDebugControl3::GetNotifyEventHandle, dbgeng/IDebugControl::GetNotifyEventHandle, debugger.getnotifyeventhandle
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
-	dbgeng.h
api_name:
-	IDebugControl.GetNotifyEventHandle
-	IDebugControl2.GetNotifyEventHandle
-	IDebugControl3.GetNotifyEventHandle
product: Windows
targetos: Windows
req.typenames: DOT4_ACTIVITY, *PDOT4_ACTIVITY
---

# IDebugControl3::GetNotifyEventHandle method


## -description


The <b>GetNotifyEventHandle</b> method receives the handle of the event that will be signaled after the next <a href="https://msdn.microsoft.com/0dd010e7-3e10-422a-adcb-8fe7df9e29ab">exception</a> in a target.


## -syntax


````
HRESULT GetNotifyEventHandle(
  [out] PULONG64 Handle
);
````


## -parameters




### -param Handle [out]

Receives the handle of the event that will be signaled.  If <i>Handle</i> is <b>NULL</b>, no event will be signaled.


## -returns



This method may also return error values.  See <a href="https://msdn.microsoft.com/713f3ee2-2f5b-415e-9908-90f5ae428b43">Return Values</a> for more details.

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
 




## -remarks



If an event to be signaled was set and an exception occurs in a target, when the engine resumes execution in the target again, the event will be signaled.

The event will only be signaled once.  After it has been signaled, this method will return <b>NULL</b> to <i>Handle</i>, unless <a href="https://msdn.microsoft.com/library/windows/hardware/ff556739">SetNotifyEventHandle</a> is called to set another event to signal. 




## -see-also

<a href="..\dbgeng\nn-dbgeng-idebugcontrol3.md">IDebugControl3</a>



<a href="..\dbgeng\nn-dbgeng-idebugcontrol.md">IDebugControl</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556739">SetNotifyEventHandle</a>



<a href="..\dbgeng\nn-dbgeng-idebugcontrol2.md">IDebugControl2</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [debugger\debugger]:%20IDebugControl::GetNotifyEventHandle method%20 RELEASE:%20(2/27/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

