---
UID: NF:ntddk.IoGetSiloParameters
title: IoGetSiloParameters function
author: windows-driver-content
description: This routine indicates if a file is within a Container context.
old-location: ifsk\iogetsiloparameters.htm
old-project: ifsk
ms.assetid: C8F42E83-2122-4871-972B-9FD06379C271
ms.author: windowsdriverdev
ms.date: 2/16/2018
ms.keywords: IoGetSiloParameters, IoGetSiloParameters function [Installable File System Drivers], PIO_FOEXT_SILO_PARAMETERS, ifsk.iogetsiloparameters, ntddk/IoGetSiloParameters
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntddk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607
req.target-min-winversvr: Windows Server 2016
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: NtosKrnl.lib
req.dll: NtosKrnl.exe
req.irql: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	NtosKrnl.exe
api_name:
-	IoGetSiloParameters
product: Windows
targetos: Windows
req.typenames: WHEA_RAW_DATA_FORMAT, *PWHEA_RAW_DATA_FORMAT
---

# IoGetSiloParameters function


## -description


This routine indicates if a file is within a Container context.


## -syntax


````
PIO_FOEXT_SILO_PARAMETERS IoGetSiloParameters(
  _In_ PFILE_OBJECT FileObject
);
````


## -parameters




### -param FileObject [in]

The file in question.


## -returns



If <b>null</b>, the file is not in a container context. Otherwise, a non-null value of type <a href="..\ntddk\ns-ntddk-_io_foext_silo_parameters.md">IO_FOEXT_SILO_PARAMETERS</a> indicates that the file is within a Container context.



