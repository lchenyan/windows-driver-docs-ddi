---
UID: NF:wudfddi.IWDFRemoteInterfaceInitialize.GetInterfaceGuid
title: IWDFRemoteInterfaceInitialize::GetInterfaceGuid method
author: windows-driver-content
description: The GetInterfaceGuid method retrieves the GUID that identifies a device interface.
old-location: wdf\iwdfremoteinterfaceinitialize_getinterfaceguid.htm
old-project: wdf
ms.assetid: 3c68d458-9b34-4e45-993a-67f915347637
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: GetInterfaceGuid method, GetInterfaceGuid method, IWDFRemoteInterfaceInitialize interface, GetInterfaceGuid,IWDFRemoteInterfaceInitialize.GetInterfaceGuid, IWDFRemoteInterfaceInitialize, IWDFRemoteInterfaceInitialize interface, GetInterfaceGuid method, IWDFRemoteInterfaceInitialize::GetInterfaceGuid, UMDFIoTargetObjectRef_bbc014c0-b69e-4109-be81-a86d93104ad4.xml, umdf.iwdfremoteinterfaceinitialize_getinterfaceguid, wdf.iwdfremoteinterfaceinitialize_getinterfaceguid, wudfddi/IWDFRemoteInterfaceInitialize::GetInterfaceGuid
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wudfddi.h
req.include-header: Wudfddi.h
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 1.9
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: Unavailable in UMDF 2.0 and later.
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: WUDFx.dll
req.irql: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	WUDFx.dll
api_name:
-	IWDFRemoteInterfaceInitialize.GetInterfaceGuid
product: Windows
targetos: Windows
req.typenames: POWER_ACTION, *PPOWER_ACTION
req.product: Windows 10 or later.
---

# IWDFRemoteInterfaceInitialize::GetInterfaceGuid method


## -description


<p class="CCE_Message">[<b>Warning:</b> UMDF 2 is the latest version of UMDF and supersedes UMDF 1.  All new UMDF drivers should be written using UMDF 2.  No new features are being added to UMDF 1 and there is limited support for UMDF 1 on newer versions of Windows 10.  Universal Windows drivers must use UMDF 2.  For more info, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/getting-started-with-umdf-version-2">Getting Started with UMDF</a>.]

The <b>GetInterfaceGuid</b> method retrieves the GUID that identifies a <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/using-device-interfaces-in-umdf-drivers">device interface</a>. 


## -syntax


````
void GetInterfaceGuid(
  [out] LPGUID pDeviceInterfaceGuid
);
````


## -parameters




### -param pDeviceInterfaceGuid [out]

A pointer to a driver-allocated GUID structure that receives the device interface GUID.


## -returns



None.




## -remarks



For more information about the <b>GetInterfaceGuid</b> method, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/using-device-interfaces-in-umdf-drivers">Using Device Interfaces in UMDF-based Drivers</a>.


#### Examples

The following code example shows how a driver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff556775">IPnpCallbackRemoteInterfaceNotification::OnRemoteInterfaceArrival</a> callback function can obtain the GUID that identifies the device interface that has arrived.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>void 
STDMETHODCALLTYPE
CMyDevice::OnRemoteInterfaceArrival(
    __in IWDFRemoteInterfaceInitialize  *FxRemoteInterfaceInit
    )
{
    GUID DeviceInterfaceGUID;
    FxRemoteInterfaceInit-&gt;GetInterfaceGuid(&amp;DeviceInterfaceGUID);
...
}</pre>
</td>
</tr>
</table></span></div>



## -see-also

<a href="..\wudfddi\nn-wudfddi-iwdfremoteinterfaceinitialize.md">IWDFRemoteInterfaceInitialize</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff560242">IWDFRemoteInterfaceInitialize::RetrieveSymbolicLink</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [wdf\wdf]:%20IWDFRemoteInterfaceInitialize::GetInterfaceGuid method%20 RELEASE:%20(2/26/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

