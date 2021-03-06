---
UID: NF:dbgeng.IDebugControl.RemoveEngineOptions
title: IDebugControl::RemoveEngineOptions method
author: windows-driver-content
description: The RemoveEngineOptions method turns off some of the engine's options.
old-location: debugger\removeengineoptions.htm
old-project: debugger
ms.assetid: ec4cf252-88c4-47de-9015-bcbbd1fd5d1d
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: IDebugControl, IDebugControl interface [Windows Debugging], RemoveEngineOptions method, IDebugControl2 interface [Windows Debugging], RemoveEngineOptions method, IDebugControl2::RemoveEngineOptions, IDebugControl3 interface [Windows Debugging], RemoveEngineOptions method, IDebugControl3::RemoveEngineOptions, IDebugControl::RemoveEngineOptions, IDebugControl_b1af0528-4fc2-4ea3-90e8-c7d92b0632f4.xml, RemoveEngineOptions method [Windows Debugging], RemoveEngineOptions method [Windows Debugging], IDebugControl interface, RemoveEngineOptions method [Windows Debugging], IDebugControl2 interface, RemoveEngineOptions method [Windows Debugging], IDebugControl3 interface, RemoveEngineOptions,IDebugControl.RemoveEngineOptions, dbgeng/IDebugControl2::RemoveEngineOptions, dbgeng/IDebugControl3::RemoveEngineOptions, dbgeng/IDebugControl::RemoveEngineOptions, debugger.removeengineoptions
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dbgeng.h
req.include-header: Dbgeng.h, Dbgeng.h, Dbgeng.h
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
-	IDebugControl.RemoveEngineOptions
-	IDebugControl2.RemoveEngineOptions
-	IDebugControl3.RemoveEngineOptions
product: Windows
targetos: Windows
req.typenames: DOT4_ACTIVITY, *PDOT4_ACTIVITY
---

# IDebugControl::RemoveEngineOptions method


## -description


The <b>RemoveEngineOptions</b> method turns off some of the engine's options.


## -syntax


````
HRESULT RemoveEngineOptions(
  [in] ULONG Options
);
````


## -parameters




### -param Options [in]

Specifies the engine options to turn off.  <i>Options</i> is a bit-set; the new value of the engine's options will equal the bitwise-NOT of <i>Options</i> combined with old value using the bitwise-AND operator (<code>new_value := old_value AND NOT Options</code>).  For a description of the engine options, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff541475">DEBUG_ENGOPT_XXX</a>.


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



After the engine options have been changed, the engine sends out notification to each client's event callback object by passing the DEBUG_CES_ENGINE_OPTIONS flag to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550683">IDebugEventCallbacks::ChangeEngineState</a> method.




## -see-also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff546598">GetEngineOptions</a>



<a href="..\dbgeng\nn-dbgeng-idebugcontrol.md">IDebugControl</a>



<a href="..\dbgeng\nn-dbgeng-idebugcontrol3.md">IDebugControl3</a>



<a href="..\dbgeng\nn-dbgeng-idebugcontrol2.md">IDebugControl2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff537884">AddEngineOptions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556670">SetEngineOptions</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [debugger\debugger]:%20IDebugControl::RemoveEngineOptions method%20 RELEASE:%20(2/27/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

