---
UID: NF:wdfcore.WDF_REL_TIMEOUT_IN_MS
title: WDF_REL_TIMEOUT_IN_MS function
author: windows-driver-content
description: The WDF_REL_TIMEOUT_IN_MS function converts a specified number of milliseconds to a relative time value.
old-location: wdf\wdf_rel_timeout_in_ms.htm
old-project: wdf
ms.assetid: f68b9575-04e4-4046-aec4-b664d8a643d4
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: DFTimerObjectRef_0504a695-4fab-4656-8522-a6c9f0989c2d.xml, WDF_REL_TIMEOUT_IN_MS, WDF_REL_TIMEOUT_IN_MS function, kmdf.wdf_rel_timeout_in_ms, wdf.wdf_rel_timeout_in_ms, wdfcore/WDF_REL_TIMEOUT_IN_MS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wdfcore.h
req.include-header: Wdf.h
req.target-type: Universal
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 1.0
req.umdf-ver: 2.0
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: None
req.dll: 
req.irql: Any level
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	LibDef
api_location:
-	None
-	None.dll
api_name:
-	WDF_REL_TIMEOUT_IN_MS
product: Windows
targetos: Windows
req.typenames: WDF_DEVICE_SHUTDOWN_FLAGS
req.product: Windows 10 or later.
---

# WDF_REL_TIMEOUT_IN_MS function


## -description


<p class="CCE_Message">[Applies to KMDF and UMDF]

The <b>WDF_REL_TIMEOUT_IN_MS</b> function converts a specified number of milliseconds to a relative time value.


## -syntax


````
LONGLONG WDF_REL_TIMEOUT_IN_MS(
  _In_ ULONGLONG Time
);
````


## -parameters




### -param Time [in]

The number of milliseconds to convert.


## -returns



<b>WDF_REL_TIMEOUT_IN_MS</b> returns the relative time value, in system time units (100-nanosecond intervals), that represents the number of milliseconds that <i>Time</i> specifies.




## -remarks



A relative time is a time value that is relative to the current system time. For example, if a caller passes a relative time value of five milliseconds to a function that accepts a time-out value, the function will time out five milliseconds after it is called.


#### Examples

The following code example starts a timer. The framework will call the timer's <a href="https://msdn.microsoft.com/abe15fd9-620e-4c24-9a82-32d20a7e49cc">EvtTimerFunc</a> callback function after ten milliseconds. 

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>BOOLEAN inTimerQueue;

inTimerQueue = WdfTimerStart(
                             timerHandle,
                             WDF_REL_TIMEOUT_IN_MS(10)
                             );</pre>
</td>
</tr>
</table></span></div>



## -see-also

<a href="..\wdfcore\nf-wdfcore-wdf_abs_timeout_in_ms.md">WDF_ABS_TIMEOUT_IN_MS</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [wdf\wdf]:%20WDF_REL_TIMEOUT_IN_MS function%20 RELEASE:%20(2/26/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

