---
UID: NE:wdm._TRACE_INFORMATION_CLASS
title: "_TRACE_INFORMATION_CLASS"
author: windows-driver-content
description: The TRACE_INFORMATION_CLASS enumeration type is used to indicate types of information associated with a WMI event tracing session.
old-location: kernel\trace_information_class.htm
old-project: kernel
ms.assetid: 38fa1687-5ad6-4536-8930-8505e5960207
ms.author: windowsdriverdev
ms.date: 3/1/2018
ms.keywords: AllLoggerHandlesClass, DiskIoNotifyRoutinesClass, EventLoggerHandleClass, FltIoNotifyRoutinesClass, GlobalLoggerHandleClass, LoggerEventsLoggedClass, LoggerEventsLostClass, MaxTraceInformationClass, TRACE_INFORMATION_CLASS, TRACE_INFORMATION_CLASS enumeration [Kernel-Mode Driver Architecture], TraceEnableFlagsClass, TraceEnableLevelClass, TraceHandleByNameClass, TraceHandleClass, TraceIdClass, TraceInformationClassReserved1, TraceInformationClassReserved2, TraceSessionSettingsClass, WdfNotifyRoutinesClass, _TRACE_INFORMATION_CLASS, kernel.trace_information_class, sysenum_a5da840d-6bda-44cb-81b3-905ece3356cd.xml, wdm/AllLoggerHandlesClass, wdm/DiskIoNotifyRoutinesClass, wdm/EventLoggerHandleClass, wdm/FltIoNotifyRoutinesClass, wdm/GlobalLoggerHandleClass, wdm/LoggerEventsLoggedClass, wdm/LoggerEventsLostClass, wdm/MaxTraceInformationClass, wdm/TRACE_INFORMATION_CLASS, wdm/TraceEnableFlagsClass, wdm/TraceEnableLevelClass, wdm/TraceHandleByNameClass, wdm/TraceHandleClass, wdm/TraceIdClass, wdm/TraceInformationClassReserved1, wdm/TraceInformationClassReserved2, wdm/TraceSessionSettingsClass, wdm/WdfNotifyRoutinesClass
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: wdm.h
req.include-header: Wdm.h, Ntddk.h, Ntifs.h
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
req.irql: PASSIVE_LEVEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wdm.h
api_name:
-	TRACE_INFORMATION_CLASS
product: Windows
targetos: Windows
req.typenames: TRACE_INFORMATION_CLASS
req.product: Windows 10 or later.
---

# _TRACE_INFORMATION_CLASS enumeration


## -description


The <b>TRACE_INFORMATION_CLASS</b> enumeration type is used to indicate types of information associated with a <a href="https://msdn.microsoft.com/library/windows/hardware/ff566350">WMI event tracing</a> session.


## -syntax


````
typedef enum _TRACE_INFORMATION_CLASS { 
  TraceIdClass                    = 0,
  TraceHandleClass,
  TraceEnableFlagsClass,
  TraceEnableLevelClass,
  GlobalLoggerHandleClass,
  EventLoggerHandleClass,
  AllLoggerHandlesClass,
  TraceHandleByNameClass,
  LoggerEventsLostClass,
  TraceSessionSettingsClass,
  LoggerEventsLoggedClass,
  DiskIoNotifyRoutinesClass,
  TraceInformationClassReserved1,
  FltIoNotifyRoutinesClass,
  TraceInformationClassReserved2,
  WdfNotifyRoutinesClass,
  MaxTraceInformationClass
} TRACE_INFORMATION_CLASS;
````


## -enum-fields




### -field TraceIdClass

Retrieves the logger ID (ULONG) of an event tracing session given a caller-supplied Wnode.


### -field TraceHandleClass

Retrieves a trace handle (TRACEHANDLE) for an event tracing session given a caller-supplied logger ID (ULONG).


### -field TraceEnableFlagsClass

Retrieves the enable flags (ULONG) set on a caller-supplied event trace handle (TRACEHANDLE).


### -field TraceEnableLevelClass

Retrieves the enable level (ULONG) set on a caller-supplied event trace handle (TRACEHANDLE).


### -field GlobalLoggerHandleClass

Retrieves an event trace handle (TRACEHANDLE) for the global logger.


### -field EventLoggerHandleClass

Reserved for use by the operating system.


### -field AllLoggerHandlesClass

Retrieves an array of event trace handles (TRACEHANDLE array) for all valid loggers.


### -field TraceHandleByNameClass

Retrieves an event trace handle (TRACEHANDLE) identified by a caller-supplied friendly name (<a href="..\wudfwdm\ns-wudfwdm-_unicode_string.md">UNICODE_STRING</a> structure in buffer).


### -field LoggerEventsLostClass

Retrieves the number (ULONG) of events lost for a logger session given a caller-supplied logger ID (ULONG).


### -field TraceSessionSettingsClass

Retrieves the settings (<b>ETW_TRACE_SESSION_SETTINGS</b> structure) for a logger session given a caller-supplied trace handle (TRACEHANDLE).


### -field LoggerEventsLoggedClass

Retrieves the number (ULONG) of events logged in a logger session given a caller-supplied logger ID (ULONG).


### -field DiskIoNotifyRoutinesClass

Reserved for use by the operating system.


### -field TraceInformationClassReserved1

Reserved for use by the operating system.


### -field FltIoNotifyRoutinesClass

Reserved for use by the operating system.


### -field TraceInformationClassReserved2

Reserved for use by the operating system.


### -field WdfNotifyRoutinesClass

Reserved for use by the operating system.


### -field MaxTraceInformationClass

The maximum value in this enumeration type.


## -remarks



<b>TRACE_INFORMATION_CLASS</b> is provided primarily for use with the <a href="..\wdm\nf-wdm-wmiquerytraceinformation.md">WmiQueryTraceInformation</a> routine, which returns information about a WMI event tracing session.




## -see-also

<a href="..\wmilib\nf-wmilib-wmifireevent.md">WmiFireEvent</a>



<a href="..\wdm\nf-wdm-wmitracemessage.md">WmiTraceMessage</a>



<a href="..\wdm\nf-wdm-wmiquerytraceinformation.md">WmiQueryTraceInformation</a>



<a href="..\wdm\nf-wdm-wmitracemessageva.md">WmiTraceMessageVa</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [kernel\kernel]:%20TRACE_INFORMATION_CLASS enumeration%20 RELEASE:%20(3/1/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

