---
UID: NF:storport.StorPortReadPortBufferUshort
title: StorPortReadPortBufferUshort macro
author: windows-driver-content
description: The StorPortReadPortBufferUshort routine reads a value from a specified port address.
old-location: storage\storportreadportbufferushort.htm
old-project: storage
ms.assetid: 7b45811c-4e5f-4344-b0b3-15d36b912b5b
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: StorPortReadPortBufferUshort, StorPortReadPortBufferUshort routine [Storage Devices], storage.storportreadportbufferushort, storport/StorPortReadPortBufferUshort, storprt_8bb9a625-864a-4566-a570-87425b6bc9af.xml
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
-	StorPortReadPortBufferUshort
product:
- Windows
targetos: Windows
req.typenames: 
---

# StorPortReadPortBufferUshort macro


## -description


The <b>StorPortReadPortBufferUshort</b> routine reads a value from a specified port address. 


## -parameters




### -param h

TBD


### -param p

TBD


### -param b

TBD


### -param c

TBD






#### - Buffer [in]

Pointer to the buffer that receives the data that is read.


#### - Count [in]

Number of data items to be read. Each data item has a size of <b>sizeof</b>(USHORT). 


#### - HwDeviceExtension [in]

Pointer to the hardware device extension.


#### - Port [in]

Pointer to the address from which to read. 


## -remarks



For more information, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff564721">ScsiPortReadPortBufferUshort</a>. For a nonbuffered version of this routine, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff567477">StorPortReadPortUshort</a>. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564721">ScsiPortReadPortBufferUshort</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff567477">StorPortReadPortUshort</a>
 

 

