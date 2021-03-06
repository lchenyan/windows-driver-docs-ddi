---
UID: NE:ntddk._WHEA_ERROR_PACKET_DATA_FORMAT
title: "_WHEA_ERROR_PACKET_DATA_FORMAT"
author: windows-driver-content
description: The WHEA_ERROR_PACKET_DATA_FORMAT enumeration defines the raw hardware error data format in a hardware error packet.
old-location: whea\whea_error_packet_data_format.htm
old-project: whea
ms.assetid: 612fbfb7-2f10-45e8-8f99-1aba8fe79a5a
ms.author: windowsdriverdev
ms.date: 2/20/2018
ms.keywords: "*PWHEA_ERROR_PACKET_DATA_FORMAT, PWHEA_ERROR_PACKET_DATA_FORMAT, PWHEA_ERROR_PACKET_DATA_FORMAT enumeration pointer [WHEA Drivers and Applications], WHEA_ERROR_PACKET_DATA_FORMAT, WHEA_ERROR_PACKET_DATA_FORMAT enumeration [WHEA Drivers and Applications], WheaDataFormatGeneric, WheaDataFormatIPFSalRecord, WheaDataFormatMax, WheaDataFormatMemory, WheaDataFormatNMIPort, WheaDataFormatPCIExpress, WheaDataFormatPCIXBus, WheaDataFormatPCIXDevice, WheaDataFormatXPFMCA, _WHEA_ERROR_PACKET_DATA_FORMAT, ntddk/PWHEA_ERROR_PACKET_DATA_FORMAT, ntddk/WHEA_ERROR_PACKET_DATA_FORMAT, ntddk/WheaDataFormatGeneric, ntddk/WheaDataFormatIPFSalRecord, ntddk/WheaDataFormatMax, ntddk/WheaDataFormatMemory, ntddk/WheaDataFormatNMIPort, ntddk/WheaDataFormatPCIExpress, ntddk/WheaDataFormatPCIXBus, ntddk/WheaDataFormatPCIXDevice, ntddk/WheaDataFormatXPFMCA, whea.whea_error_packet_data_format, whearef_19f75c8f-94d0-4837-ab44-e9ba9fbe51f7.xml"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: ntddk.h
req.include-header: Ntddk.h
req.target-type: Windows
req.target-min-winverclnt: Supported in Windows 7 and later versions of Windows.
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
-	ntddk.h
api_name:
-	WHEA_ERROR_PACKET_DATA_FORMAT
product: Windows
targetos: Windows
req.typenames: WHEA_ERROR_PACKET_DATA_FORMAT, *PWHEA_ERROR_PACKET_DATA_FORMAT
---

# _WHEA_ERROR_PACKET_DATA_FORMAT enumeration


## -description


The WHEA_ERROR_PACKET_DATA_FORMAT enumeration defines the raw hardware error data format in a hardware error packet.


## -syntax


````
typedef enum _WHEA_ERROR_PACKET_DATA_FORMAT { 
  WheaDataFormatIPFSalRecord  = 0,
  WheaDataFormatXPFMCA,
  WheaDataFormatMemory,
  WheaDataFormatPCIExpress,
  WheaDataFormatNMIPort,
  WheaDataFormatPCIXBus,
  WheaDataFormatPCIXDevice,
  WheaDataFormatGeneric,
  WheaDataFormatMax
} WHEA_ERROR_PACKET_DATA_FORMAT, *PWHEA_ERROR_PACKET_DATA_FORMAT;
````


## -enum-fields




### -field WheaDataFormatIPFSalRecord

The raw data in the hardware error packet contains an Itanium processor family system abstraction layer (SAL) error record. For more information about the format of a SAL error record, see the <a href="http://go.microsoft.com/fwlink/p/?linkid=72212">Intel Itanium Processor Family System Abstraction Layer Specification</a>.


### -field WheaDataFormatXPFMCA

The raw data in the hardware error packet is formatted as an MCA_EXCEPTION structure. For more information about the MCA_EXCEPTION structure, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff540659">HalQuerySystemInformation</a>.


### -field WheaDataFormatMemory

The raw data in the hardware error packet contains memory error data. The format of this error data is dependent on the memory architecture.


### -field WheaDataFormatPCIExpress

The raw data in the hardware error packet is formatted as a <a href="https://msdn.microsoft.com/library/windows/hardware/ff537457">PCI_EXPRESS_AER_CAPABILITY</a> structure.


### -field WheaDataFormatNMIPort

The raw data in the hardware error packet contains the data that was read from the nonmaskable interrupt (NMI) I/O ports by the NMI low-level hardware error handler (LLHEH). The format of this error data is specific to the implementation.


### -field WheaDataFormatPCIXBus

The raw data in the hardware error packet contains PCI/PCI-X bus error data. The format of this error data is specific to the implementation.


### -field WheaDataFormatPCIXDevice

The raw data in the hardware error packet contains a PCI/PCI-X device error data. The format of this error data is specific to the implementation.


### -field WheaDataFormatGeneric

The raw data in the hardware error packet is formatted as a <a href="..\ntddk\ns-ntddk-_whea_generic_error.md">WHEA_GENERIC_ERROR</a> structure.


### -field WheaDataFormatMax

The maximum number of formats of raw hardware error data.


## -remarks



The <a href="..\ntddk\ns-ntddk-_whea_error_packet_v2.md">WHEA_ERROR_PACKET_V2</a> structure contains a member of type WHEA_ERROR_PACKET_DATA_FORMAT that specifies the format of the raw data that is contained in the hardware error packet.




## -see-also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff537457">PCI_EXPRESS_AER_CAPABILITY</a>



<a href="..\ntddk\ns-ntddk-_whea_generic_error.md">WHEA_GENERIC_ERROR</a>



<a href="..\ntddk\ns-ntddk-_whea_error_packet_v2.md">WHEA_ERROR_PACKET_V2</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [whea\whea]:%20WHEA_ERROR_PACKET_DATA_FORMAT enumeration%20 RELEASE:%20(2/20/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

