---
UID: NS:pep_x._PEP_WORK_ACPI_EVALUATE_CONTROL_METHOD_COMPLETE
title: "_PEP_WORK_ACPI_EVALUATE_CONTROL_METHOD_COMPLETE"
author: windows-driver-content
description: The PEP_WORK_ACPI_EVALUATE_CONTROL_METHOD_COMPLETE structure contains the results of an ACPI control method that was asynchronously evaluated by the platform extension plug-in (PEP).
old-location: kernel\pep_work_acpi_evaluate_control_method_complete.htm
old-project: kernel
ms.assetid: 76D45B13-03C2-4B57-98B5-9E527ADCC72F
ms.author: windowsdriverdev
ms.date: 3/1/2018
ms.keywords: "*PPEP_WORK_ACPI_EVALUATE_CONTROL_METHOD_COMPLETE, PEP_WORK_ACPI_EVALUATE_CONTROL_METHOD_COMPLETE, PEP_WORK_ACPI_EVALUATE_CONTROL_METHOD_COMPLETE structure [Kernel-Mode Driver Architecture], PPEP_WORK_ACPI_EVALUATE_CONTROL_METHOD_COMPLETE, PPEP_WORK_ACPI_EVALUATE_CONTROL_METHOD_COMPLETE structure pointer [Kernel-Mode Driver Architecture], _PEP_WORK_ACPI_EVALUATE_CONTROL_METHOD_COMPLETE, kernel.pep_work_acpi_evaluate_control_method_complete, pepfx/PEP_WORK_ACPI_EVALUATE_CONTROL_METHOD_COMPLETE, pepfx/PPEP_WORK_ACPI_EVALUATE_CONTROL_METHOD_COMPLETE"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: pep_x.h
req.include-header: Pep_x.h
req.target-type: Windows
req.target-min-winverclnt: Supported starting with Windows 10.
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
req.irql: PASSIVE_LEVEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	pepfx.h
api_name:
-	PEP_WORK_ACPI_EVALUATE_CONTROL_METHOD_COMPLETE
product: Windows
targetos: Windows
req.typenames: PEP_WORK_ACPI_EVALUATE_CONTROL_METHOD_COMPLETE, *PPEP_WORK_ACPI_EVALUATE_CONTROL_METHOD_COMPLETE, PEP_WORK_ACPI_EVALUATE_CONTROL_METHOD_COMPLETE, *PPEP_WORK_ACPI_EVALUATE_CONTROL_METHOD_COMPLETE
---

# _PEP_WORK_ACPI_EVALUATE_CONTROL_METHOD_COMPLETE structure


## -description


The <b>PEP_WORK_ACPI_EVALUATE_CONTROL_METHOD_COMPLETE</b> structure contains the results of an ACPI control method that was asynchronously evaluated by the platform extension plug-in (PEP).


## -syntax


````
typedef struct _PEP_WORK_ACPI_EVALUATE_CONTROL_METHOD_COMPLETE {
  POHANDLE              DeviceHandle;
  ULONG                 CompletionFlags;
  PVOID                 CompletionContext;
  SIZE_T                OutputArgumentSize;
  PACPI_METHOD_ARGUMENT OutputArguments;
} PEP_WORK_ACPI_EVALUATE_CONTROL_METHOD_COMPLETE, *PPEP_WORK_ACPI_EVALUATE_CONTROL_METHOD_COMPLETE;
````


## -struct-fields




### -field DeviceHandle

A POHANDLE value that represents the registration of the device with the Windows <a href="https://msdn.microsoft.com/B08F8ABF-FD43-434C-A345-337FBB799D9B">power management framework</a> (PoFx). The PEP previously received this handle from PoFx during the <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/mt186689">PEP_NOTIFY_ACPI_REGISTER_DEVICE</a> notification in which the PEP elected to provide ACPI services for the device.


### -field CompletionFlags

A set of completion flags. No flags are currently defined for this member, which is always set to PEP_ACPI_EVALUATE_CONTROL_METHOD_COMPLETE_FLAG_NONE (0x0).


### -field MethodStatus

 


### -field CompletionContext

A pointer to a completion context value. This is the same pointer that PoFx passed to the PEP in the <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/mt186659">PEP_NOTIFY_ACPI_EVALUATE_CONTROL_METHOD</a> notification that initiated the asynchronous evaluation of the ACPI control method.


### -field OutputArgumentSize

The size, in bytes, of the buffer pointed to by the <b>OutputArguments</b> member.


### -field OutputArguments

A pointer to a buffer to which the PEP has written the result of evaluating the ACPI control method. This buffer starts with a <a href="..\acpiioct\ns-acpiioct-_acpi_method_argument_v1.md">ACPI_METHOD_ARGUMENT</a> structure, which might be followed by additional output data. PoFx allocated this buffer and passed the buffer pointer to the PEP in the <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/mt186659">PEP_NOTIFY_ACPI_EVALUATE_CONTROL_METHOD</a> notification that initiated the asynchronous evaluation of the ACPI control method.


## -remarks



The <b>ControlMethodComplete</b> member of the <a href="..\pepfx\ns-pepfx-_pep_work_information.md">PEP_WORK_INFORMATION</a> structure is a <b>PEP_WORK_ACPI_EVALUATE_CONTROL_METHOD_COMPLETE</b> structure.

A <b>PEP_WORK_INFORMATION</b> structure is included in the input parameters to the <a href="https://msdn.microsoft.com/library/windows/hardware/mt186629">CompleteWork</a> routine. The PEP writes the control method results to the <b>ControlMethodComplete</b> member of this structure before calling the routine. Evaluation of the control method was initiated by a previous <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/mt186659">PEP_NOTIFY_ACPI_EVALUATE_CONTROL_METHOD</a> notification.




## -see-also

<a href="..\pepfx\ns-pepfx-_pep_work_information.md">PEP_WORK_INFORMATION</a>



<a href="https://msdn.microsoft.com/en-us/library/windows/hardware/mt186689">PEP_NOTIFY_ACPI_REGISTER_DEVICE</a>



<a href="..\acpiioct\ns-acpiioct-_acpi_method_argument_v1.md">ACPI_METHOD_ARGUMENT</a>



<a href="https://msdn.microsoft.com/en-us/library/windows/hardware/mt186659">PEP_NOTIFY_ACPI_EVALUATE_CONTROL_METHOD</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [kernel\kernel]:%20PEP_WORK_ACPI_EVALUATE_CONTROL_METHOD_COMPLETE structure%20 RELEASE:%20(3/1/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

