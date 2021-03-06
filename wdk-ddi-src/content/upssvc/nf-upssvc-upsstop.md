---
UID: NF:upssvc.UPSStop
title: UPSStop function
author: windows-driver-content
description: The UPSStop function causes a UPS minidriver to stop monitoring its UPS unit.
old-location: battery\upsstop.htm
old-project: battery
ms.assetid: 55555e58-eaba-4c39-a771-9924da3fcfc4
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: UPSStop, UPSStop function [Battery Devices], UPS_fns_60f920b5-6225-4569-a60a-dfb1c6b2538c.xml, battery.upsstop, upssvc/UPSStop
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: upssvc.h
req.include-header: Upssvc.h
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
-	HeaderDef
api_location:
-	Upssvc.h
api_name:
-	UPSStop
product: Windows
targetos: Windows
req.typenames: UMDETW_ALLOCATION_USAGE
req.product: Windows 10 or later.
---

# UPSStop function


## -description


The <b>UPSStop</b> function causes a UPS minidriver to stop monitoring its UPS unit.


## -syntax


````
void UPSStop(
   void 
);
````


## -parameters








## -returns



None




## -remarks



The <b>UPSStop</b> function must:

<ul>
<li>
Cancel all waiting calls to <a href="..\upssvc\nf-upssvc-upswaitforstatechange.md">UPSWaitForStateChange</a>.

</li>
<li>
Stop monitoring the UPS unit.

</li>
<li>
Close and release the UPS unit's COM port.

</li>
</ul>
After <b>UPSStop</b> returns, the only function the UPS service can call is <a href="..\upssvc\nf-upssvc-upsinit.md">UPSInit</a>. 




## -see-also

<a href="..\upssvc\nf-upssvc-upsinit.md">UPSInit</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [battery\battery]:%20UPSStop function%20 RELEASE:%20(2/15/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

