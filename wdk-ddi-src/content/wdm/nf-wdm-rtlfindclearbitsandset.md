---
UID: NF:wdm.RtlFindClearBitsAndSet
title: RtlFindClearBitsAndSet function
author: windows-driver-content
description: The RtlFindClearBitsAndSet routine searches for a range of clear bits of a requested size within a bitmap and sets all bits in the range when it has been located.
old-location: kernel\rtlfindclearbitsandset.htm
old-project: kernel
ms.assetid: 9558e2bc-4975-4b32-8e95-9fc5e0f7882e
ms.author: windowsdriverdev
ms.date: 3/1/2018
ms.keywords: RtlFindClearBitsAndSet, RtlFindClearBitsAndSet routine [Kernel-Mode Driver Architecture], k109_187055d4-54ce-4ede-878a-fd97079e6fdd.xml, kernel.rtlfindclearbitsandset, wdm/RtlFindClearBitsAndSet
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wdm.h
req.include-header: Wdm.h, Ntddk.h, Ntifs.h
req.target-type: Universal
req.target-min-winverclnt: Available starting with Windows 2000.
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
req.lib: NtosKrnl.lib
req.dll: NtosKrnl.exe
req.irql: "<= APC_LEVEL (See Remarks section)"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	NtosKrnl.exe
api_name:
-	RtlFindClearBitsAndSet
product: Windows
targetos: Windows
req.typenames: WORK_QUEUE_TYPE
req.product: Windows 10 or later.
---

# RtlFindClearBitsAndSet function


## -description


The <b>RtlFindClearBitsAndSet</b> routine searches for a range of clear bits of a requested size within a bitmap and sets all bits in the range when it has been located. 


## -syntax


````
ULONG RtlFindClearBitsAndSet(
  _In_ PRTL_BITMAP BitMapHeader,
  _In_ ULONG       NumberToFind,
  _In_ ULONG       HintIndex
);
````


## -parameters




### -param BitMapHeader [in]

A pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff563614">RTL_BITMAP</a> structure that describes the bitmap. This structure must have been initialized by the <a href="..\wdm\nf-wdm-rtlinitializebitmap.md">RtlInitializeBitMap</a> routine. 


### -param NumberToFind [in]

Specifies how many contiguous clear bits will satisfy this request. 


### -param HintIndex [in]

Specifies a zero-based bit position from which to start looking for a clear bit range of the given size. 


## -returns



<b>RtlFindClearBitsAndSet</b> either returns the zero-based starting bit index for a clear bit range of the requested size that it set, or it returns 0xFFFFFFFF if it cannot find such a range within the given bitmap variable. 




## -remarks



For a successful call, the returned bit position is not necessarily equivalent to the given <i>HintIndex</i>. If necessary, <b>RtlFindClearBitsAndSet</b> searches the whole bitmap to locate a clear bit range of the requested size. However, it starts searching for the requested range from <i>HintIndex</i>, so callers can have such a range reset more quickly when they can supply appropriate hints about where to start looking.

Callers of <b>RtlFindClearBitsAndSet</b> must be running at IRQL &lt;= APC_LEVEL if the memory that contains the bitmap variable is pageable or the memory at <i>BitMapHeader</i> is pageable. Otherwise, <b>RtlFindClearBitsAndSet</b> can be called at any IRQL.




## -see-also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff563614">RTL_BITMAP</a>



<a href="..\wdm\nf-wdm-rtlinitializebitmap.md">RtlInitializeBitMap</a>



<a href="..\wdm\nf-wdm-rtlfindfirstrunclear.md">RtlFindFirstRunClear</a>



<a href="..\wdm\nf-wdm-rtlfindclearbits.md">RtlFindClearBits</a>



<a href="..\wdm\nf-wdm-rtlsetallbits.md">RtlSetAllBits</a>



<a href="..\wdm\nf-wdm-rtlarebitsclear.md">RtlAreBitsClear</a>



<a href="..\wdm\nf-wdm-rtlnumberofclearbits.md">RtlNumberOfClearBits</a>



<a href="..\wdm\nf-wdm-rtlfindclearruns.md">RtlFindClearRuns</a>



<a href="..\wdm\nf-wdm-rtlfindlastbackwardrunclear.md">RtlFindLastBackwardRunClear</a>



<a href="..\wdm\nf-wdm-rtlfindlongestrunclear.md">RtlFindLongestRunClear</a>



<a href="..\wdm\nf-wdm-rtlsetbits.md">RtlSetBits</a>



<a href="..\wdm\nf-wdm-rtlfindnextforwardrunclear.md">RtlFindNextForwardRunClear</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [kernel\kernel]:%20RtlFindClearBitsAndSet routine%20 RELEASE:%20(3/1/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

