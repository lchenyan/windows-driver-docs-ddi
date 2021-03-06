---
UID: NF:dbgeng.IDebugClient5.ConnectProcessServerWide
title: IDebugClient5::ConnectProcessServerWide method
author: windows-driver-content
description: The ConnectProcessServerWide method connects to a process server.
old-location: debugger\connectprocessserverwide.htm
old-project: debugger
ms.assetid: 42979da6-d044-4d52-858f-98871c3941bc
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: ConnectProcessServerWide method [Windows Debugging], ConnectProcessServerWide method [Windows Debugging], IDebugClient5 interface, ConnectProcessServerWide,IDebugClient5.ConnectProcessServerWide, IDebugClient5, IDebugClient5 interface [Windows Debugging], ConnectProcessServerWide method, IDebugClient5::ConnectProcessServerWide, dbgeng/IDebugClient5::ConnectProcessServerWide, debugger.connectprocessserverwide
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
-	IDebugClient5.ConnectProcessServerWide
product: Windows
targetos: Windows
req.typenames: DOT4_ACTIVITY, *PDOT4_ACTIVITY
---

# IDebugClient5::ConnectProcessServerWide method


## -description


The <b>ConnectProcessServerWide</b> method connects to a <a href="https://msdn.microsoft.com/4cfad26c-d8c0-4f80-aa54-b9cadbc84df3">process server</a>.


## -syntax


````
HRESULT ConnectProcessServerWide(
  [in]  PCWSTR   RemoteOptions,
  [out] PULONG64 Server
);
````


## -parameters




### -param RemoteOptions [in]

Specifies how the <a href="https://msdn.microsoft.com/e4d53375-c82e-493b-9ccb-444c211fbc79">debugger engine</a> will connect with the process server.  These are the same options passed to the <b>-premote</b> option on the WinDbg and CDB command lines.  For details on the syntax of this string, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff537840">Activating a Smart Client</a>.


### -param Server [out]

Receives a handle for the process server.  This handle is used when creating or attaching to processes by using the process server.


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



For more information about process servers and remote debugging, see <a href="https://msdn.microsoft.com/ed7ea3dc-07d1-481c-90e0-7f0b0e77ad42">Process Servers, Kernel Connection Servers, and Smart Clients</a>.




## -see-also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff548254">GetRunningProcessSystemIdByExecutableName</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff539323">CreateProcess2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff542993">EndProcessServer</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541969">DisconnectProcessServer</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff548265">GetRunningProcessSystemIds</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540055">CreateProcessAndAttach2</a>



<a href="..\dbgeng\nn-dbgeng-idebugclient5.md">IDebugClient5</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff558810">StartProcessServer</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff548243">GetRunningProcessDescription</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538150">AttachProcess</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [debugger\debugger]:%20IDebugClient5::ConnectProcessServerWide method%20 RELEASE:%20(2/27/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

