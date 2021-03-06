---
UID: NS:usbfnbase._ALTERNATE_INTERFACE
title: "_ALTERNATE_INTERFACE"
author: windows-driver-content
description: The ALTERNATE_INTERFACE structure provides information about alternate settings for a Universal Serial Bus (USB) interface.
old-location: buses\alternate_interface.htm
old-project: usbref
ms.assetid: F57FA113-F664-4B10-8457-DF6D266264E9
ms.author: windowsdriverdev
ms.date: 2/24/2018
ms.keywords: "*PALTERNATE_INTERFACE, ALTERNATE_INTERFACE, ALTERNATE_INTERFACE structure [Buses], PALTERNATE_INTERFACE, PALTERNATE_INTERFACE structure pointer [Buses], _ALTERNATE_INTERFACE, buses.alternate_interface, usbfnbase/ALTERNATE_INTERFACE, usbfnbase/PALTERNATE_INTERFACE"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: usbfnbase.h
req.include-header: Usbfnbase.h
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
-	usbfnbase.h
api_name:
-	ALTERNATE_INTERFACE
product: Windows
targetos: Windows
req.typenames: ALTERNATE_INTERFACE, *PALTERNATE_INTERFACE
req.product: Windows 10 or later.
---

# _ALTERNATE_INTERFACE structure


## -description


The <b>ALTERNATE_INTERFACE</b> structure provides information about alternate settings for a Universal Serial Bus (USB) interface.


## -syntax


````
typedef struct _ALTERNATE_INTERFACE {
  USHORT InterfaceNumber;
  USHORT AlternateInterfaceNumber;
} ALTERNATE_INTERFACE, *PALTERNATE_INTERFACE;
````


## -struct-fields




### -field InterfaceNumber

The index number for theUSB interface setting.


### -field AlternateInterfaceNumber

The index number for the alternate USB interface setting.


## -see-also

<a href="..\usbfnbase\ns-usbfnbase-_usbfn_notification.md">USBFN_NOTIFICATION</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [usbref\buses]:%20ALTERNATE_INTERFACE structure%20 RELEASE:%20(2/24/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

