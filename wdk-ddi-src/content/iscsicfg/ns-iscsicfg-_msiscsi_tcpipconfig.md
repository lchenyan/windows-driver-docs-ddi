---
UID: NS:iscsicfg._MSiSCSI_TCPIPConfig
title: "_MSiSCSI_TCPIPConfig"
author: windows-driver-content
description: The MSiSCSI_TCPIPConfig structure reports TCP/IP configuration information about one of the adapter's ports.
old-location: storage\msiscsi_tcpipconfig.htm
old-project: storage
ms.assetid: 1f33d262-0488-46cb-a762-1f3e24cdd219
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: "*PMSiSCSI_TCPIPConfig, MSiSCSI_TCPIPConfig, MSiSCSI_TCPIPConfig structure [Storage Devices], PMSiSCSI_TCPIPConfig, PMSiSCSI_TCPIPConfig structure pointer [Storage Devices], _MSiSCSI_TCPIPConfig, iscsicfg/MSiSCSI_TCPIPConfig, iscsicfg/PMSiSCSI_TCPIPConfig, storage.msiscsi_tcpipconfig, structs-iSCSI_4ca5e222-7926-4646-a915-014cf20caed1.xml"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: iscsicfg.h
req.include-header: Iscsicfg.h
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
-	iscsicfg.h
api_name:
-	MSiSCSI_TCPIPConfig
product: Windows
targetos: Windows
req.typenames: MSiSCSI_TCPIPConfig, *PMSiSCSI_TCPIPConfig
---

# _MSiSCSI_TCPIPConfig structure


## -description


The MSiSCSI_TCPIPConfig structure reports TCP/IP configuration information about one of the adapter's ports. 


## -syntax


````
typedef struct _MSiSCSI_TCPIPConfig {
  BOOLEAN          UseLinkLocalAddress;
  BOOLEAN          EnableDHCP;
  BOOLEAN          UseDHCPForDNS;
  ULONG            IPVersions;
  ISCSI_IP_Address IpAddress;
  ISCSI_IP_Address DefaultGateway;
  ISCSI_IP_Address SubnetMask;
  ISCSI_IP_Address PreferredDNSServer;
  ISCSI_IP_Address AlternateDNSServer;
} MSiSCSI_TCPIPConfig, *PMSiSCSI_TCPIPConfig;
````


## -struct-fields




### -field UseLinkLocalAddress

A Boolean value that indicates whether the HBA should use an autogenerated and non-routable (link local) address as its IP address. If this member is <b>TRUE</b>, the HBA should use an autogenerated and non-routable (link local) address as its IP address. If this member is <b>FALSE</b>, the HBA is not required to use a link local address.


### -field EnableDHCP

A Boolean value that indicates whether the HBA should use DHCP to discover IP address information. If this member is <b>TRUE</b>, the HBA should use DHCP to discover IP address information. If this member is <b>FALSE</b>, the HBA is not required to use DHCP to discover IP address information.


### -field UseDHCPForDNS

A Boolean value that indicates whether the HBA should use DHCP to discover DNS addresses. If this member is <b>TRUE</b>, the HBA should use DHCP to discover DNS addresses. If <b>FALSE</b>, the HBA is not required to use DHCP to discover DNS addresses.


### -field IPVersions

The version of the IP protocol that the HBA supports. A value of 0x00000001 indicates that the HBA supports version 4 of the IP protocol, and a value of 0x00000002 indicates that the HBA supports version 6.


### -field IpAddress

A <a href="..\iscsidef\ns-iscsidef-_iscsi_ip_address.md">ISCSI_IP_Address</a> structure that specifies the IP address for the HBA. The ISCSI_IP_Address structure provides a version-independent way of defining the IP address.


### -field DefaultGateway

A <a href="..\iscsidef\ns-iscsidef-_iscsi_ip_address.md">ISCSI_IP_Address</a> structure that specifies the static IP address for the default gateway. The ISCSI_IP_Address structure provides a version-independent way of defining the IP address of the default gateway.


### -field SubnetMask

A <a href="..\iscsidef\ns-iscsidef-_iscsi_ip_address.md">ISCSI_IP_Address</a> structure that specifies the static subnet mask. The ISCSI_IP_Address structure provides a version-independent way of defining the subnet mask.


### -field PreferredDNSServer

A <a href="..\iscsidef\ns-iscsidef-_iscsi_ip_address.md">ISCSI_IP_Address</a> structure that specifies the IP address of the preferred DNS server. The ISCSI_IP_Address structure provides a version-independent way of defining the IP address of the preferred DNS server.


### -field AlternateDNSServer

A <a href="..\iscsidef\ns-iscsidef-_iscsi_ip_address.md">ISCSI_IP_Address</a> structure that specifies the IP address of the alternate DNS server. The ISCSI_IP_Address structure provides a version-independent way of defining the IP address of the alternate DNS server.


## -remarks



The WMI tool suite automatically generates a declaration of the MSiSCSI_TCPIPConfig structure when it compiles the <a href="https://msdn.microsoft.com/library/windows/hardware/ff563151">MSiSCSI_TCPIPConfig WMI Class</a> in <i>Config.mof</i>.You must implement this class.




## -see-also

<a href="..\iscsidef\ns-iscsidef-_iscsi_ip_address.md">ISCSI_IP_Address</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563151">MSiSCSI_TCPIPConfig WMI Class</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [storage\storage]:%20MSiSCSI_TCPIPConfig structure%20 RELEASE:%20(2/26/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

