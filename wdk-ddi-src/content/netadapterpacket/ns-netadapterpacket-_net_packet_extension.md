---
UID: NS:netadapterpacket._NET_PACKET_EXTENSION
title: _NET_PACKET_EXTENSION
author: windows-driver-content
description: The NET_PACKET_EXTENSION structure contains packet extension information for either a net adapter or a datapath queue.
ms.assetid: 39383b7d-e36d-42cd-8766-ac681375e3e0
ms.author: windowsdriverdev
ms.date: 02/21/2018
ms.topic: struct
ms.prod: windows-hardware
ms.technology: windows-devices
ms.keywords: _NET_PACKET_EXTENSION, NET_PACKET_EXTENSION, *PNET_PACKET_EXTENSION, 
req.header: netadapterpacket.h
req.include-header: netadaptercx.h
req.target-type:
req.target-min-winverclnt:
req.target-min-winversvr:
req.kmdf-ver: 1.25
req.umdf-ver:
req.lib:
req.dll:
req.ddi-compliance:
req.unicode-ansi:
req.max-support:
req.typenames: NET_PACKET_EXTENSION, *PNET_PACKET_EXTENSION
topictype: 
-	apiref
apitype: 
-	HeaderDef
apilocation: 
-	netadapterpacket.h
apiname: 
-	_NET_PACKET_EXTENSION
product: Windows
targetos: Windows
---

# _NET_PACKET_EXTENSION structure

## -description
> [!WARNING]
> Some information in this topic relates to prereleased product, which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.
>
> NetAdapterCx is preview only in Windows 10, version 1803.

The **NET_PACKET_EXTENSION** structure describes a packet extension for either a net adapter or one of its datapath queues.

## -struct-fields

### -field Size
The size of this structure, in bytes.
 
### -field Name
The name of the packet extension.
 
### -field Version
The version of the packet extension.
 
### -field Alignment
The alignment requirement for the extension.
 
### -field ExtensionSize
The size, in bytes, of the packet extension.

## -remarks
Call [NET_PACKET_EXTENSION_INIT](nf-netadapterpacket-net_packet_extension_init.md) to initialize this structure.

This structure represents a packet extension itself, whereas the similar [NET_PACKET_EXTENSION_QUERY](ns-netadapterpacket-_net_packet_extension_query.md) structure represents a query for that extension.

For more information about packet extensions and available packet extension constants, see [Packet descriptors and extensions](https://docs.microsoft.com/windows-hardware/drivers/netcx/packet-descriptors-and-extensions). For a code sample, see *[EvtNetAdapterCreateTxQueue](../netadapter/nc-netadapter-evt_net_adapter_create_txqueue.md)* or *[EvtNetAdapterCreateRxQueue](../netadapter/nc-netadapter-evt_net_adapter_create_rxqueue.md)*.

The minimum NetAdapterCx version for **NET_PACKET_EXTENSION** is 1.2.

## -see-also