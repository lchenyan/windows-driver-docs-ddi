---
UID: NS:miniport._PCI_EXPRESS_LINK_STATUS_REGISTER
title: "_PCI_EXPRESS_LINK_STATUS_REGISTER"
author: windows-driver-content
description: The PCI_EXPRESS_LINK_STATUS_REGISTER structure describes a PCI Express (PCIe) link status register of a PCIe capability structure.
old-location: pci\pci_express_link_status_register.htm
old-project: PCI
ms.assetid: c3431e89-4a47-44e6-98d8-eae444ea1915
ms.author: windowsdriverdev
ms.date: 2/24/2018
ms.keywords: "*PPCI_EXPRESS_LINK_STATUS_REGISTER, PCI.pci_express_link_status_register, PCI_EXPRESS_LINK_STATUS_REGISTER, PCI_EXPRESS_LINK_STATUS_REGISTER union [Buses], PPCI_EXPRESS_LINK_STATUS_REGISTER, PPCI_EXPRESS_LINK_STATUS_REGISTER union pointer [Buses], _PCI_EXPRESS_LINK_STATUS_REGISTER, ntddk/PCI_EXPRESS_LINK_STATUS_REGISTER, ntddk/PPCI_EXPRESS_LINK_STATUS_REGISTER, pci_struct_41d11df3-521f-4709-a30e-be70ad36db8f.xml"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: miniport.h
req.include-header: Ntddk.h, Miniport.h
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
req.irql: Any level (see Remarks section)
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ntddk.h
api_name:
-	PCI_EXPRESS_LINK_STATUS_REGISTER
product: Windows
targetos: Windows
req.typenames: PCI_EXPRESS_LINK_STATUS_REGISTER, *PPCI_EXPRESS_LINK_STATUS_REGISTER
---

# _PCI_EXPRESS_LINK_STATUS_REGISTER structure


## -description


The PCI_EXPRESS_LINK_STATUS_REGISTER structure describes a PCI Express (PCIe) link status register of a PCIe capability structure.


## -syntax


````
typedef union _PCI_EXPRESS_LINK_STATUS_REGISTER {
  struct {
    USHORT LinkSpeed  :4;
    USHORT LinkWidth  :6;
    USHORT Undefined  :1;
    USHORT LinkTraining  :1;
    USHORT SlotClockConfig  :1;
    USHORT DataLinkLayerActive  :1;
    USHORT Rsvd  :2;
  };
  USHORT AsUSHORT;
} PCI_EXPRESS_LINK_STATUS_REGISTER, *PPCI_EXPRESS_LINK_STATUS_REGISTER;
````


## -struct-fields




### -field DUMMYSTRUCTNAME

 


### -field AsUSHORT

A USHORT representation of the contents of the PCI_EXPRESS_LINK_STATUS_REGISTER structure.


#### - DataLinkLayerActive

A single bit that indicates that the data link control and management state machine is in the data link active state.


#### - LinkSpeed

The negotiated link speed of the PCIe link.  Possible values are:

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td><b>1</b></td>
<td>2.5 gigabits per second.</td>
</tr>
<tr>
<td><b>2</b></td>
<td>5.0 gigabits per second.</td>
</tr>
<tr>
<td>All other values</td>
<td>Reserved.</td>
</tr>
</table>
 


#### - LinkTraining

A single bit that indicates that the link is in the configuration or recovery state, or that a 1 was written to the retrain link bit of the PCIe link control register and the training has not yet begun. This member is not applicable to endpoint devices and upstream ports of switches.


#### - LinkWidth

The negotiated link width (number of lanes) of the PCIe link. Possible values are:

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td><b>1</b></td>
<td>x1 (1 lane)</td>
</tr>
<tr>
<td><b>2</b></td>
<td>x2 (2 lanes)</td>
</tr>
<tr>
<td><b>4</b></td>
<td>x4 (4 lanes)</td>
</tr>
<tr>
<td><b>8</b></td>
<td>x8 (8 lanes)</td>
</tr>
<tr>
<td><b>12</b></td>
<td>x12 (12 lanes)</td>
</tr>
<tr>
<td><b>16</b></td>
<td>x16 (16 lanes)</td>
</tr>
<tr>
<td><b>32</b></td>
<td>x32 (32 lanes)</td>
</tr>
<tr>
<td>All other values</td>
<td>Reserved.</td>
</tr>
</table>
 


#### - Rsvd

Reserved.


#### - SlotClockConfig

A single bit that indicates that the component uses the same physical reference clock that the hardware platform provides on the PCIe slot connector. If this bit is clear, the component uses an independent clock irrespective of the presence of a reference clock on the PCIe slot connector.


#### - Undefined

Reserved. Device drivers and other system software should ignore any value read from this bit.


## -remarks



The PCI_EXPRESS_LINK_STATUS_REGISTER structure is available in Windows Server 2008 and later versions of Windows.

A PCI_EXPRESS_LINK_STATUS_REGISTER structure is contained in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff537460">PCI_EXPRESS_CAPABILITY</a> structure.




## -see-also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff537460">PCI_EXPRESS_CAPABILITY</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [PCI\buses]:%20PCI_EXPRESS_LINK_STATUS_REGISTER union%20 RELEASE:%20(2/24/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

