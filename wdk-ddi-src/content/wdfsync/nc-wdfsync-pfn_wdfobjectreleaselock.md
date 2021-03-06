---
UID: NC:wdfsync.PFN_WDFOBJECTRELEASELOCK
title: PFN_WDFOBJECTRELEASELOCK
author: windows-driver-content
description: The WdfObjectReleaseLock method releases an object's synchronization lock.
old-location: wdf\wdfobjectreleaselock.htm
old-project: wdf
ms.assetid: a2fe9393-1525-47d7-94e1-1886ea54e270
ms.author: windowsdriverdev
ms.date: 1/11/2018
ms.keywords: wdf.wdfobjectreleaselock, PFN_WDFOBJECTRELEASELOCK, WdfObjectReleaseLock callback function, WdfObjectReleaseLock, wdfsync/WdfObjectReleaseLock, DFSynchroRef_14ab9c69-1eb8-4a83-b1fb-cb8db7a67d06.xml, kmdf.wdfobjectreleaselock
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: wdfsync.h
req.include-header: Wdf.h
req.target-type: Universal
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 1.0
req.umdf-ver: 2.0
req.ddi-compliance: DriverCreate, KmdfIrql, KmdfIrql2
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: "<=DISPATCH_LEVEL"
topictype:
-	APIRef
-	kbSyntax
apitype:
-	UserDefined
apilocation:
-	wdfsync.h
apiname:
-	WdfObjectReleaseLock
product: Windows
targetos: Windows
req.typenames: "*PWDF_REQUEST_SEND_OPTIONS, WDF_REQUEST_SEND_OPTIONS"
req.product: Windows 10 or later.
---

# PFN_WDFOBJECTRELEASELOCK callback


## -description


<p class="CCE_Message">[Applies to KMDF and UMDF]

The <b>WdfObjectReleaseLock</b> method releases an object's synchronization lock.


## -prototype


````
VOID WdfObjectReleaseLock(
  _In_ WDFOBJECT Object
);
````


## -parameters




### -param DriverGlobals



### -param WDFOBJECT






#### - Object [in]

A handle to a framework device object or a framework queue object.


## -returns


None.

A bug check occurs if the driver supplies an invalid object handle.





## -remarks


The <b>WdfObjectReleaseLock</b> method releases the synchronization lock that a driver acquired by previously calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff548721">WdfObjectAcquireLock</a>. <b>WdfObjectReleaseLock</b> also restores the driver's IRQL to the value that it had before the driver called <b>WdfObjectAcquireLock</b>.

For more information about synchronization locks, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/synchronization-techniques-for-wdf-drivers">Synchronization Techniques for Framework-Based Drivers</a>.



## -see-also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff548721">WdfObjectAcquireLock</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [wdf\wdf]:%20WdfObjectReleaseLock callback function%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

