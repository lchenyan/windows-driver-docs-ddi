---
UID: NI:bthioctl.IOCTL_BTH_GET_RADIO_INFO
title: IOCTL_BTH_GET_RADIO_INFO
author: windows-driver-content
description: The IOCTL_BTH_GET_RADIO_INFO request obtains information about the specified remote radio.
old-location: bltooth\ioctl_bth_get_radio_info.htm
old-project: bltooth
ms.assetid: 45803e80-6090-4b64-8c92-6b5efebd1cfc
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IOCTL_BTH_GET_RADIO_INFO, IOCTL_BTH_GET_RADIO_INFO control code [Bluetooth Devices], bltooth.ioctl_bth_get_radio_info, bth_ioctls_ed6699c7-3a05-46bd-ba8b-d138ce1ad751.xml, bthioctl/IOCTL_BTH_GET_RADIO_INFO
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: ioctl
req.header: bthioctl.h
req.include-header: Bthioctl.h
req.target-type: Windows
req.target-min-winverclnt: Versions:\_Supported in Windows Vista, and later.
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
req.irql: "<= PASSIVE_LEVEL"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Bthioctl.h
api_name:
-	IOCTL_BTH_GET_RADIO_INFO
product: Windows
targetos: Windows
req.typenames: HFP_BYPASS_CODEC_ID_V1, *PHFP_BYPASS_CODEC_ID_V1
---

# IOCTL_BTH_GET_RADIO_INFO IOCTL


## -description



The IOCTL_BTH_GET_RADIO_INFO request obtains information about the specified remote radio.




## -ioctlparameters




### -input-buffer

The 
      <b>AssociatedIrp.SystemBuffer</b> member specifies the Bluetooth address of the remote radio to
      query.


### -input-buffer-length

The length of the buffer.


### -output-buffer

The 
      <b>AssociatedIrp.SystemBuffer</b> member points to a buffer that holds a 
      <a href="..\bthioctl\ns-bthioctl-_bth_radio_info.md">BTH_RADIO_INFO</a> structure. This structure
      contains information about the remote radio's feature support for the Link Management Protocol (LMP),
      the radio's manufacturer ID, and its LMP version.


### -output-buffer-length

The length of a 
      <a href="..\bthioctl\ns-bthioctl-_bth_radio_info.md">BTH_RADIO_INFO</a> structure. 


### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block

If the request is successful, the 
      <b>Information</b> member of the STATUS_BLOCK structure is set to the size, in bytes, of the output
      buffer. Otherwise, the 
      <b>Information</b> member is set to zero.

The 
      <b>Status</b> member is set to one of the values in the following table.

<table>
<tr>
<th>Status value</th>
<th>Description</th>
</tr>
<tr>
<td>
STATUS_SUCCESS

</td>
<td>
The IOCTL completed successfully.

</td>
</tr>
<tr>
<td>
STATUS_DEVICE_NOT_CONNECTED

</td>
<td>
The device object for the specified device was not connected.

</td>
</tr>
</table>
 


## -remarks



The IOCTL_BTH_GET_RADIO_INFO IOCTL returns similar information as the IOCTL_BTH_GET_LOCAL_INFO IOCTL,
    but for a remote Bluetooth radio.




## -see-also

<a href="..\bthioctl\ns-bthioctl-_bth_radio_info.md">BTH_RADIO_INFO</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [bltooth\bltooth]:%20IOCTL_BTH_GET_RADIO_INFO control code%20 RELEASE:%20(2/15/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

