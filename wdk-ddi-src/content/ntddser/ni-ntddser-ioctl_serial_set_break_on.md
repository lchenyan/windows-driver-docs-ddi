---
UID: NI:ntddser.IOCTL_SERIAL_SET_BREAK_ON
title: IOCTL_SERIAL_SET_BREAK_ON
author: windows-driver-content
description: The IOCTL_SERIAL_SET_BREAK_ON request sets the line control break signal active.
old-location: serports\ioctl_serial_set_break_on.htm
old-project: serports
ms.assetid: bee9cb3c-0ccd-4304-ba7e-7896a16ab123
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IOCTL_SERIAL_SET_BREAK_ON, IOCTL_SERIAL_SET_BREAK_ON control code [Serial Ports], ntddser/IOCTL_SERIAL_SET_BREAK_ON, serports.ioctl_serial_set_break_on, serref_47487a08-4b73-4e3a-be2e-4343dd678b44.xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: ioctl
req.header: ntddser.h
req.include-header: Ntddser.h
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
-	Ntddser.h
api_name:
-	IOCTL_SERIAL_SET_BREAK_ON
product: Windows
targetos: Windows
req.typenames: SD_REQUEST_FUNCTION
---

# IOCTL_SERIAL_SET_BREAK_ON IOCTL


## -description


The <b>IOCTL_SERIAL_SET_BREAK_ON</b> request sets the line control break signal active.

To set the line control break signal inactive, a client can use an <a href="..\ntddser\ni-ntddser-ioctl_serial_set_break_off.md">IOCTL_SERIAL_SET_BREAK_OFF</a> request.


## -ioctlparameters




### -input-buffer

None.


### -input-buffer-length

None.


### -output-buffer

None.


### -output-buffer-length

None.


### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block

The <b>Information</b> member is set to zero.

The <b>Status</b> member is set to one of the <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/serports/serial-device-control-requests2">Generic Status Values for Serial Device Control Requests</a>.


## -see-also

<a href="..\ntddser\ni-ntddser-ioctl_serial_set_break_off.md">IOCTL_SERIAL_SET_BREAK_OFF</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [serports\serports]:%20IOCTL_SERIAL_SET_BREAK_ON control code%20 RELEASE:%20(2/15/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

