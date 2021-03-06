---
UID: NC:ndis.NDIS_PD_ALLOCATE_COUNTER
title: NDIS_PD_ALLOCATE_COUNTER
author: windows-driver-content
description: The PacketDirect (PD) platform calls a PD-capable miniport driver's NdisPDAllocateCounter function to allocate a counter object.
old-location: netvista\ndispdallocatecounter.htm
old-project: netvista
ms.assetid: 86AA537D-952F-4A7A-ACA4-24B8C1AE932A
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: NDIS_PD_ALLOCATE_COUNTER, NdisPDAllocateCounter, NdisPDAllocateCounter callback function [Network Drivers Starting with Windows Vista], ndis/NdisPDAllocateCounter, netvista.ndispdallocatecounter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: ndis.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: Windows Server 2016
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
req.irql: PASSIVE_LEVEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Ndis.h
api_name:
-	NdisPDAllocateCounter
product: Windows
targetos: Windows
req.typenames: VIDEO_STREAM_INIT_PARMS, *LPVIDEO_STREAM_INIT_PARMS
---

# NDIS_PD_ALLOCATE_COUNTER callback


## -description


The PacketDirect (PD) platform calls a PD-capable miniport driver's 
   <i>NdisPDAllocateCounter</i> function to allocate a counter object. There are three kinds of counters:<ul>
<li>
Receive queue counters are used for tracking receive queue activity.

</li>
<li>
Transmit queue counters are used for tracking transmit queue activity.

</li>
<li>
Filter counters are used for tracking filter match activity.

</li>
</ul>
<div class="alert"><b>Note</b>  You must declare the function by using the <b>NDIS_PD_ALLOCATE_COUNTER</b> type. For more
   information, see the following Examples section.</div>
<div> </div>



## -prototype


````
NDIS_PD_ALLOCATE_COUNTER NdisPDAllocateCounter;

NTSTATUS NdisPDAllocateCounter(
  _In_        NDIS_PD_PROVIDER_HANDLE    ProviderHandle,
  _In_  const NDIS_PD_COUNTER_PARAMETERS *CounterParameters,
  _Out_       NDIS_PD_COUNTER_HANDLE     *CounterHandle
)
{ ... }
````


## -parameters




### -param ProviderHandle [in]

A provider handle that identifies the PD-capable miniport driver's provider object.


### -param CounterParameters [in]

An <a href="..\ndis\ns-ndis-_ndis_pd_counter_parameters.md">NDIS_PD_COUNTER_PARAMETERS</a> structure that specifies information such as the counter type.


### -param CounterHandle [out]

A pointer to a driver-allocated counter handle variable. If the counter allocation succeeds, the miniport driver returns a handle to the newly allocated counter in this variable.


## -returns



<i>NdisPDAllocateCounter</i> can return one of the following status values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The miniport driver successfully allocated the counter and returned a handle in the <i>CounterHandle</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INSUFFICIENT_RESOURCES</b></dt>
</dl>
</td>
<td width="60%">
 The allocation failed due to insufficient resources.

</td>
</tr>
</table>
 




## -remarks



The same counter object can be associated with multiple  queue or filter objects of the same  type as the counter. For example, if there are  5 receive queues (RQ1 through RQ5) and 2 receive counters (RC1 and RC2), receive counter RC1 could be associated with receive queues RQ1, RQ2, RQ3, and receive counter RC2 could be associated with receive queues RQ4 and RQ5.

<h3><a id="Examples"></a><a id="examples"></a><a id="EXAMPLES"></a>Examples</h3>
To define a <i>NdisPDAllocateCounter</i> function, you must first provide a function declaration that identifies the type of function you're defining. Windows provides a set of function types for drivers. Declaring a function using the function types helps <a href="https://msdn.microsoft.com/2F3549EF-B50F-455A-BDC7-1F67782B8DCA">Code Analysis for Drivers</a>, <a href="https://msdn.microsoft.com/74feeb16-387c-4796-987a-aff3fb79b556">Static Driver Verifier</a> (SDV), and other verification tools find errors, and it's a requirement for writing drivers for the Windows operating system.

For example, to define a <i>NdisPDAllocateCounter</i> function that is named "MyPDAllocateCounter", use the <b>NDIS_PD_ALLOCATE_COUNTER</b> type as shown in this code example:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>NDIS_PD_ALLOCATE_COUNTER MyPDAllocateCounter;</pre>
</td>
</tr>
</table></span></div>
Then, implement your function as follows:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>_Use_decl_annotations_
NTSTATUS
 MyPDAllocateCounter(
    NDIS_PD_PROVIDER_HANDLE  ProviderHandle,
    CONST NDIS_PD_COUNTER_PARAMETERS*  CounterParameters,
    NDIS_PD_COUNTER_HANDLE*  CounterHandle
    )
  {...}</pre>
</td>
</tr>
</table></span></div>
The <b>NDIS_PD_ALLOCATE_COUNTER</b> function type is defined in the Ntddndis.h header file. To more accurately identify errors when you run the code analysis tools, be sure to add the _Use_decl_annotations_ annotation to your function definition.  The _Use_decl_annotations_ annotation ensures that the annotations that are applied to the <b>NDIS_PD_ALLOCATE_COUNTER</b> function type in the header file are used.  For more information about the requirements for function declarations, see <a href="https://msdn.microsoft.com/232c4272-0bf0-4a4e-9560-3bceeca8a3e3">Declaring Functions by Using Function Role Types for NDIS Drivers</a>.

For information about  _Use_decl_annotations_, see <a href="http://go.microsoft.com/fwlink/p/?linkid=286697">Annotating Function Behavior</a>. 




## -see-also

<a href="..\ndis\nc-ndis-ndis_pd_free_counter.md">NdisPDFreeCounter</a>



<a href="..\ndis\ns-ndis-_ndis_pd_counter_parameters.md">NDIS_PD_COUNTER_PARAMETERS</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20NDIS_PD_ALLOCATE_COUNTER callback function%20 RELEASE:%20(2/27/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

