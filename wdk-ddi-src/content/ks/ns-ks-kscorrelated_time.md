---
UID: NS:ks.KSCORRELATED_TIME
title: KSCORRELATED_TIME
author: windows-driver-content
description: The KSCORRELATED_TIME structure contains a clock time as well as the corresponding number of clock ticks since system boot.
old-location: stream\kscorrelated_time.htm
old-project: stream
ms.assetid: d733f50c-01a2-484f-ab5b-72aaa3378c7d
ms.author: windowsdriverdev
ms.date: 2/23/2018
ms.keywords: "*PKSCORRELATED_TIME, KSCORRELATED_TIME, KSCORRELATED_TIME structure [Streaming Media Devices], PKSCORRELATED_TIME, PKSCORRELATED_TIME structure pointer [Streaming Media Devices], ks-struct_4bc7b067-fc0e-4343-9ae9-4bfe5aec90e3.xml, ks/KSCORRELATED_TIME, ks/PKSCORRELATED_TIME, stream.kscorrelated_time"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ks.h
req.include-header: Ks.h
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
-	HeaderDef
api_location:
-	ks.h
api_name:
-	KSCORRELATED_TIME
product: Windows
targetos: Windows
req.typenames: KSCORRELATED_TIME, *PKSCORRELATED_TIME
---

# KSCORRELATED_TIME structure


## -description


The KSCORRELATED_TIME structure contains a clock time as well as the corresponding number of clock ticks since system boot.


## -syntax


````
typedef struct {
  LONGLONG Time;
  LONGLONG SystemTime;
} KSCORRELATED_TIME, *PKSCORRELATED_TIME;
````


## -struct-fields




### -field Time

Specifies the current clock time in 100-nanosecond units.


### -field SystemTime

A 64-bit integer containing the number of clock ticks since system boot.


## -remarks



Supply this structure in a <a href="https://msdn.microsoft.com/library/windows/hardware/ff564465">KSPROPERTY_CLOCK_CORRELATEDTIME</a> property request.

The system time is acquired from <a href="..\wdm\nf-wdm-kequeryperformancecounter.md">KeQueryPerformanceCounter</a>. Note that the performance counter is not suspended when the machine is suspended, so that correlations change when the machine goes through a suspend.




## -see-also

<a href="..\wdm\nf-wdm-kequeryperformancecounter.md">KeQueryPerformanceCounter</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564465">KSPROPERTY_CLOCK_CORRELATEDTIME</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [stream\stream]:%20KSCORRELATED_TIME structure%20 RELEASE:%20(2/23/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

