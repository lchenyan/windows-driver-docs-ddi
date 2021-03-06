---
UID: NS:iscsiop._SetCHAPSharedSecret_OUT
title: "_SetCHAPSharedSecret_OUT"
author: windows-driver-content
description: The SetCHAPSharedSecret_OUT structure holds the output data for the SetCHAPSharedSecret method.
old-location: storage\setchapsharedsecret_out.htm
old-project: storage
ms.assetid: a169a5b2-5303-41fc-80d2-69b44fd45c47
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: "*PSetCHAPSharedSecret_OUT, PSetCHAPSharedSecret_OUT, PSetCHAPSharedSecret_OUT structure pointer [Storage Devices], SetCHAPSharedSecret_OUT, SetCHAPSharedSecret_OUT structure [Storage Devices], _SetCHAPSharedSecret_OUT, iscsiop/PSetCHAPSharedSecret_OUT, iscsiop/SetCHAPSharedSecret_OUT, storage.setchapsharedsecret_out, structs-iSCSI_f11f03d2-424a-4537-9cbd-f4fd3ca0e59d.xml"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: iscsiop.h
req.include-header: Iscsiop.h
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
-	iscsiop.h
api_name:
-	SetCHAPSharedSecret_OUT
product: Windows
targetos: Windows
req.typenames: SetCHAPSharedSecret_OUT, *PSetCHAPSharedSecret_OUT
---

# _SetCHAPSharedSecret_OUT structure


## -description


The SetCHAPSharedSecret_OUT structure holds the output data for the <a href="https://msdn.microsoft.com/library/windows/hardware/ff565585">SetCHAPSharedSecret</a> method.


## -syntax


````
typedef struct _SetCHAPSharedSecret_OUT {
  ULONG Status;
} SetCHAPSharedSecret_OUT, *PSetCHAPSharedSecret_OUT;
````


## -struct-fields




### -field Status

On output, the status of the <b>SetCHAPSharedSecret</b> operation. For a list of status qualifiers, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff561568">ISCSI_STATUS_QUALIFIERS</a>.  


## -remarks



You must implement this method.




## -see-also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff561568">ISCSI_STATUS_QUALIFIERS</a>



<a href="..\iscsiop\ns-iscsiop-_setchapsharedsecret_in.md">SetCHAPSharedSecret_IN</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565585">SetCHAPSharedSecret</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [storage\storage]:%20SetCHAPSharedSecret_OUT structure%20 RELEASE:%20(2/26/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

