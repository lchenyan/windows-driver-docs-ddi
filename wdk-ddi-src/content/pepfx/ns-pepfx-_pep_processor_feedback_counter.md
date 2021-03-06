---
UID: NS:pepfx._PEP_PROCESSOR_FEEDBACK_COUNTER
title: "_PEP_PROCESSOR_FEEDBACK_COUNTER"
author: windows-driver-content
description: The PEP_PROCESSOR_FEEDBACK_COUNTER structure describes a feedback counter to the operating system.
old-location: kernel\pep_processor_feedback_counter.htm
old-project: kernel
ms.assetid: 275AE285-6309-4A03-A02C-DBE8D44727CE
ms.author: windowsdriverdev
ms.date: 3/1/2018
ms.keywords: "*PPEP_PROCESSOR_FEEDBACK_COUNTER, PEP_PROCESSOR_FEEDBACK_COUNTER, PEP_PROCESSOR_FEEDBACK_COUNTER structure [Kernel-Mode Driver Architecture], PPEP_PROCESSOR_FEEDBACK_COUNTER, PPEP_PROCESSOR_FEEDBACK_COUNTER structure pointer [Kernel-Mode Driver Architecture], PROCESSOR_FEEDBACK_COUNTER_FREQUENCY, PROCESSOR_FEEDBACK_COUNTER_PERFORMANCE, PROCESSOR_FEEDBACK_TYPE_INSTANTANEOUS, PROCESSOR_FEEDBACK_TYPE_RELATIVE, _PEP_PROCESSOR_FEEDBACK_COUNTER, kernel.pep_processor_feedback_counter, pepfx/PEP_PROCESSOR_FEEDBACK_COUNTER, pepfx/PPEP_PROCESSOR_FEEDBACK_COUNTER"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: pepfx.h
req.include-header: Pep_x.h
req.target-type: Windows
req.target-min-winverclnt: Supported starting with Windows 10.
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
req.irql: PASSIVE_LEVEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	pepfx.h
api_name:
-	PEP_PROCESSOR_FEEDBACK_COUNTER
product: Windows
targetos: Windows
req.typenames: PEP_PROCESSOR_FEEDBACK_COUNTER, *PPEP_PROCESSOR_FEEDBACK_COUNTER
---

# _PEP_PROCESSOR_FEEDBACK_COUNTER structure


## -description


The <b>PEP_PROCESSOR_FEEDBACK_COUNTER</b> structure describes a feedback counter to the operating system.


## -syntax


````
typedef struct _PEP_PROCESSOR_FEEDBACK_COUNTER {
  struct {
    ULONG Affinitized  :1;
    ULONG Type  :2;
    ULONG Counter  :4;
    ULONG Reserved  :25;
  };
  ULONG  NominalRate;
} PEP_PROCESSOR_FEEDBACK_COUNTER, *PPEP_PROCESSOR_FEEDBACK_COUNTER;
````


## -struct-fields




### -field NominalRate

Specifies the nominal rate of the counter. 


#### - Affinitized

Identifies the counter process affinity. If set to 1, the counter must be read while executing on the target processor, otherwise, it will be set to 0.


#### - Counter

Specifies the data the counter is providing.


The processor feedback counter types are:



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PROCESSOR_FEEDBACK_COUNTER_FREQUENCY_"></a><a id="processor_feedback_counter_frequency_"></a><dl>
<dt><b>PROCESSOR_FEEDBACK_COUNTER_FREQUENCY </b></dt>
<dt>0x00</dt>
</dl>
</td>
<td width="60%">
The feedback counter returns the clock speed of the processor. The nominal rate is the nominal clock speed, in MHz.

</td>
</tr>
<tr>
<td width="40%"><a id="PROCESSOR_FEEDBACK_COUNTER_PERFORMANCE"></a><a id="processor_feedback_counter_performance"></a><dl>
<dt><b>PROCESSOR_FEEDBACK_COUNTER_PERFORMANCE</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
The feedback counter returns the current processor performance. The nominal rate is equivalent to the processorâ€™s <b>NominalPerformance</b> (see <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/mt186825">PEP_NOTIFY_PPM_QUERY_PERF_CAPABILITIES notification</a>).

</td>
</tr>
</table>
 


#### - Reserved

This member is reserved and should be set to zero.


#### - Type

Specifies the data type of the counter.


The processor feedback counter data types are:



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PROCESSOR_FEEDBACK_TYPE_INSTANTANEOUS"></a><a id="processor_feedback_type_instantaneous"></a><dl>
<dt><b>PROCESSOR_FEEDBACK_TYPE_INSTANTANEOUS</b></dt>
<dt>0x00</dt>
</dl>
</td>
<td width="60%">
The feedback counter returns the instantaneous value of the property being counted.

</td>
</tr>
<tr>
<td width="40%"><a id="PROCESSOR_FEEDBACK_TYPE_RELATIVE"></a><a id="processor_feedback_type_relative"></a><dl>
<dt><b>PROCESSOR_FEEDBACK_TYPE_RELATIVE</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
The feedback counter returns two incrementing values: the nominal count, and the actual count. Nominal count increments at a fixed nominal rate. Actual count increments at a variable rate relative to the property being counted. When the property is incrementing at its nominal rate, the two values should increment at the same rate. To compute an average rate over a time period, the OS reads the counter once and the beginning of the period and once at the end and computes:

<img alt="The average rate is equal to the nominal rate multiplied by the quotient of the variable rate divided by the fixed rate." src="../Common/PEP_PROCESSOR_FEEDBACK_COUNTER_equation.png"/>

</td>
</tr>
</table>
 


## -remarks



This structure 




## -see-also

<a href="https://msdn.microsoft.com/478E1AB1-B888-4EC2-A9C3-A33475E499E3">PEP structures</a>



<a href="https://msdn.microsoft.com/en-us/library/windows/hardware/mt186825">PEP_NOTIFY_PPM_QUERY_PERF_CAPABILITIES notification</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [kernel\kernel]:%20PEP_PROCESSOR_FEEDBACK_COUNTER structure%20 RELEASE:%20(3/1/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

