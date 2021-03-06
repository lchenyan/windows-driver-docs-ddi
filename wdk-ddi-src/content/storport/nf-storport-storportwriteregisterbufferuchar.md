---
UID: NF:storport.StorPortWriteRegisterBufferUchar
title: StorPortWriteRegisterBufferUchar macro
author: windows-driver-content
description: The StorPortWriteRegisterBufferUchar routine transfers a given number of unsigned bytes from a buffer to the HBA.
old-location: storage\storportwriteregisterbufferuchar.htm
old-project: storage
ms.assetid: af8126cd-e931-4106-b543-9c84ee110901
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: StorPortWriteRegisterBufferUchar, StorPortWriteRegisterBufferUchar routine [Storage Devices], storage.storportwriteregisterbufferuchar, storport/StorPortWriteRegisterBufferUchar, storprt_21fa4636-6492-4cb1-9281-6f116f1a7591.xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: storport.h
req.include-header: Storport.h
req.target-type: Universal
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
req.lib: Storport.lib
req.dll: 
req.irql: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	LibDef
api_location:
-	Storport.lib
-	Storport.dll
api_name:
-	StorPortWriteRegisterBufferUchar
product: Windows
targetos: Windows
req.typenames: STOR_SPINLOCK
req.product: Windows 10 or later.
---

# StorPortWriteRegisterBufferUchar macro


## -description


The <b>StorPortWriteRegisterBufferUchar</b> routine transfers a given number of unsigned bytes from a buffer to the HBA. 


## -syntax


````
VOID StorPortWriteRegisterBufferUchar(
   IN PVOID  HwDeviceExtension,
   IN PUCHAR Register,
   IN ULONG  Count
);
````


## -parameters




### -param h

TBD


### -param r

TBD


### -param b

TBD


### -param c

TBD






#### - Count

Specifies the number of bytes to be transferred to the HBA. 


#### - HwDeviceExtension

A pointer to the hardware device extension. This is a per HBA storage area that the port driver allocates and initializes on behalf of the miniport driver. Miniport drivers usually store HBA-specific information in this extension, such as the state of the HBA and the mapped access ranges for the HBA. This area is available to the miniport driver immediately after the miniport driver calls <a href="..\storport\nf-storport-storportinitialize.md">StorPortInitialize</a>. The port driver frees this memory when it removes the device. 


#### - Register

Pointer to a buffer containing the data to be written. 


## -see-also

<a href="..\storport\nf-storport-scsiportwriteregisterbufferuchar.md">ScsiPortWriteRegisterBufferUchar</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [storage\storage]:%20StorPortWriteRegisterBufferUchar routine%20 RELEASE:%20(2/26/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

