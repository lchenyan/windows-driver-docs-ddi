---
UID: NF:prnasntp.IBidiAsyncNotifyChannel.AsyncGetNotificationSendResponse
title: IBidiAsyncNotifyChannel::AsyncGetNotificationSendResponse method
author: windows-driver-content
description: "."
old-location: print\ibidiasyncnotifychannel_asyncgetnotificationsendresponse.htm
old-project: print
ms.assetid: F30A1DEA-2B54-417A-AFE7-289655C815E2
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: AsyncGetNotificationSendResponse method [Print Devices], AsyncGetNotificationSendResponse method [Print Devices], IBidiAsyncNotifyChannel interface, AsyncGetNotificationSendResponse,IBidiAsyncNotifyChannel.AsyncGetNotificationSendResponse, IBidiAsyncNotifyChannel, IBidiAsyncNotifyChannel interface [Print Devices], AsyncGetNotificationSendResponse method, IBidiAsyncNotifyChannel::AsyncGetNotificationSendResponse, print.ibidiasyncnotifychannel_asyncgetnotificationsendresponse, prnasntp/IBidiAsyncNotifyChannel::AsyncGetNotificationSendResponse
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: prnasntp.h
req.include-header: 
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
-	COM
api_location:
-	Prnasntp.h
api_name:
-	IBidiAsyncNotifyChannel.AsyncGetNotificationSendResponse
product: Windows
targetos: Windows
req.typenames: USERDATA, *PUSERDATA
req.product: Windows 10 or later.
---

# IBidiAsyncNotifyChannel::AsyncGetNotificationSendResponse method


## -description





## -syntax


````
HRESULT AsyncGetNotificationSendResponse(
  [in] IPrintAsyncNotifyDataObject     *pObject,
  [in] IAsyncGetSendNotificationCookie *pCookie
);
````


## -parameters




### -param param




### -param EQUALNULL






#### - pCookie [in]


#### - pObject [in]


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also

<a href="..\prnasntp\nn-prnasntp-ibidiasyncnotifychannel.md">IBidiAsyncNotifyChannel</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [print\print]:%20IBidiAsyncNotifyChannel::AsyncGetNotificationSendResponse method%20 RELEASE:%20(2/26/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

