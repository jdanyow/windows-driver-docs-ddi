---
UID: NF:ndis.NdisMCompleteDmaTransfer
title: NdisMCompleteDmaTransfer macro
author: windows-driver-content
description: The NdisMCompleteDmaTransfer function indicates that a system DMA transfer operation has completed. It resets the system DMA controller in preparation for further DMA transfers.
old-location: netvista\ndismcompletedmatransfer.htm
old-project: netvista
ms.assetid: 12a8062a-6d4b-4757-a076-56aeb5e4e48c
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: NdisMCompleteDmaTransfer, NdisMCompleteDmaTransfer macro [Network Drivers Starting with Windows Vista], dma_ref_bd601fef-cf06-42ff-9906-d3bf8edef72f.xml, ndis/NdisMCompleteDmaTransfer, netvista.ndismcompletedmatransfer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: ndis.h
req.include-header: Ndis.h
req.target-type: Universal
req.target-min-winverclnt: Supported for NDIS 6.0 and NDIS 5.1 drivers (see    NdisMCompleteDmaTransfer (NDIS   5.1)) in Windows Vista. Supported for NDIS 5.1 drivers (see    NdisMCompleteDmaTransfer (NDIS   5.1)) in Windows XP.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: Irql_MCO_Function
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: "<= DISPATCH_LEVEL"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ndis.h
api_name:
-	NdisMCompleteDmaTransfer
product:
- Windows
targetos: Windows
req.typenames: 
---

# NdisMCompleteDmaTransfer macro


## -description


The 
  <b>NdisMCompleteDmaTransfer</b> function indicates that a system DMA transfer operation has completed. It
  resets the system DMA controller in preparation for further DMA transfers.


## -parameters




### -param _S

TBD


### -param _H

TBD


### -param _B

TBD


### -param _O

TBD


### -param _L

TBD


### -param _M_

TBD






#### - Buffer [in]

A pointer to the buffer descriptor previously passed to 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff563675">NdisMSetupDmaTransfer</a>.


#### - Length [in]

The length in bytes of the transfer. This value also was passed to 
     <b>NdisMSetupDmaTransfer</b>.


#### - MiniportDmaHandle [in]

The handle returned when the 
     <a href="https://msdn.microsoft.com/b146fa81-005b-4a6c-962d-4cb023ea790e">MiniportInitializeEx</a> function
     called the 
     <a href="https://msdn.microsoft.com/32e92f77-8f45-408b-a284-c00d3b5bd1b4">
     NdisMRegisterDmaChannel</a> function.


#### - Offset [in]

The byte offset at which the transfer began. This value also was passed to 
     <b>NdisMSetupDmaTransfer</b>.


#### - Status [out]

A pointer to a caller-supplied variable in which this function returns the final status of the DMA
     transfer, which can be one of the following:
     





#### NDIS_STATUS_SUCCESS

The data has been transferred and flushed to host memory or to the device to maintain data
       integrity.



#### NDIS_STATUS_RESOURCES

The DMA controller was released but the data transfer might be incoherent.


#### - WriteToDevice [in]

<b>TRUE</b> if the transfer was from the host to the NIC, as, for example, a send operation.


## -remarks



<b>NdisMCompleteDmaTransfer</b> must be called with 
    <i>WriteToDevice</i> set to <b>TRUE</b> before the transferred data is considered present in the NIC's memory. 
    <b>NdisMCompleteDmaTransfer</b> must be called with 
    <i>WriteToDevice</i> set to <b>FALSE</b> before the transferred data can be read from host memory.




## -see-also




<a href="https://msdn.microsoft.com/b146fa81-005b-4a6c-962d-4cb023ea790e">MiniportInitializeEx</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563646">NdisMRegisterDmaChannel</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563675">NdisMSetupDmaTransfer</a>
 

 

