---
UID: NI:usbfnioctl.IOCTL_INTERNAL_USBFN_SET_POWER_FILTER_EXIT_LPM
title: IOCTL_INTERNAL_USBFN_SET_POWER_FILTER_EXIT_LPM
author: windows-driver-content
description: Do not use.
old-location: buses\ioctl_internal_usbfn_set_power_filter_exit_lpm.htm
old-project: usbref
ms.assetid: 2A3A1723-989E-44FD-9727-7A01218652D1
ms.author: windowsdriverdev
ms.date: 2/24/2018
ms.keywords: IOCTL_INTERNAL_USBFN_SET_POWER_FILTER_EXIT_LPM, IOCTL_INTERNAL_USBFN_SET_POWER_FILTER_EXIT_LPM control code [Buses], buses.ioctl_internal_usbfn_set_power_filter_exit_lpm, usbfnioctl/IOCTL_INTERNAL_USBFN_SET_POWER_FILTER_EXIT_LPM
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: ioctl
req.header: usbfnioctl.h
req.include-header: Usbfnioctl.h
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
-	usbfnioctl.h
api_name:
-	IOCTL_INTERNAL_USBFN_SET_POWER_FILTER_EXIT_LPM
product: Windows
targetos: Windows
req.typenames: USBFN_USB_STRING, *PUSBFN_USB_STRING
req.product: Windows 10 or later.
---

# IOCTL_INTERNAL_USBFN_SET_POWER_FILTER_EXIT_LPM IOCTL


## -description


Do not use.


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



Irp->IoStatus.Status is set to STATUS_SUCCESS if the request is successful.

Otherwise, Status to the appropriate error condition as a NTSTATUS code. 

For more information, see [NTSTATUS Values](https://docs.microsoft.com/en-us/windows-hardware/drivers/kernel/ntstatus-values).




## -remarks



This request must be sent after sending the  <a href="..\usbfnioctl\ni-usbfnioctl-ioctl_internal_usbfn_activate_usb_bus.md">IOCTL_INTERNAL_USBFN_ACTIVATE_USB_BUS</a> request.

Upon receiving this request, the filter driver
    communicates with the hardware and brings the controller out of LPM.




## -see-also

<a href="https://msdn.microsoft.com/library/windows/hardware/dn379336">Link Power management in USB 3.0 Hardware</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [usbref\buses]:%20IOCTL_INTERNAL_USBFN_SET_POWER_FILTER_EXIT_LPM control code%20 RELEASE:%20(2/24/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

