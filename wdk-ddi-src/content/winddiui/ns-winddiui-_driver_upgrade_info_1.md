---
UID: NS:winddiui._DRIVER_UPGRADE_INFO_1
title: "_DRIVER_UPGRADE_INFO_1"
author: windows-driver-content
description: The DRIVER_UPGRADE_INFO_1 structure is used as an input to a printer interface DLL's DrvUpgradePrinter function.
old-location: print\driver_upgrade_info_1.htm
old-project: print
ms.assetid: fef7c63b-ca9e-47f4-96cb-4dafa080ddcf
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: "*PDRIVER_UPGRADE_INFO_1, DRIVER_UPGRADE_INFO_1, DRIVER_UPGRADE_INFO_1 structure [Print Devices], PDRIVER_UPGRADE_INFO_1, PDRIVER_UPGRADE_INFO_1 structure pointer [Print Devices], _DRIVER_UPGRADE_INFO_1, print.driver_upgrade_info_1, print_interface-graphics_eb7333cb-f073-4c0b-ade4-20a477d28f67.xml, winddiui/DRIVER_UPGRADE_INFO_1, winddiui/PDRIVER_UPGRADE_INFO_1"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winddiui.h
req.include-header: Winddiui.h
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
-	winddiui.h
api_name:
-	DRIVER_UPGRADE_INFO_1
product: Windows
targetos: Windows
req.typenames: DRIVER_UPGRADE_INFO_1, *PDRIVER_UPGRADE_INFO_1
req.product: Windows 10 or later.
---

# _DRIVER_UPGRADE_INFO_1 structure


## -description


The DRIVER_UPGRADE_INFO_1 structure is used as an input to a printer interface DLL's <a href="..\winddiui\nf-winddiui-drvupgradeprinter.md">DrvUpgradePrinter</a> function.


## -syntax


````
typedef struct _DRIVER_UPGRADE_INFO_1 {
  LPTSTR pPrinterName;
  LPTSTR pOldDriverDirectory;
} DRIVER_UPGRADE_INFO_1, *PDRIVER_UPGRADE_INFO_1;
````


## -struct-fields




### -field pPrinterName

Pointer to a NULL-terminated string that specifies the name of the printer.


### -field pOldDriverDirectory

Pointer to a NULL-terminated string that specifies the local directory in which the old printer driver files can be found.


## -see-also

<a href="..\winddiui\ns-winddiui-_driver_upgrade_info_2.md">DRIVER_UPGRADE_INFO_2</a>



<a href="..\winddiui\nf-winddiui-drvupgradeprinter.md">DrvUpgradePrinter</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [print\print]:%20DRIVER_UPGRADE_INFO_1 structure%20 RELEASE:%20(2/26/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

