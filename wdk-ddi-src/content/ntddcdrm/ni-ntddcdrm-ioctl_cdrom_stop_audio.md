---
UID: NI:ntddcdrm.IOCTL_CDROM_STOP_AUDIO
title: IOCTL_CDROM_STOP_AUDIO
author: windows-driver-content
description: Ends audio play. Obsolete, beginning with Windows Vista.
old-location: storage\ioctl_cdrom_stop_audio.htm
old-project: storage
ms.assetid: 9d250950-7ecf-4433-9aaf-7696abb5b66c
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: IOCTL_CDROM_STOP_AUDIO, IOCTL_CDROM_STOP_AUDIO control, IOCTL_CDROM_STOP_AUDIO control code [Storage Devices], k307_f800aa8a-b12c-4373-9e6a-0b2a12182540.xml, ntddcdrm/IOCTL_CDROM_STOP_AUDIO, storage.ioctl_cdrom_stop_audio
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: ioctl
req.header: ntddcdrm.h
req.include-header: Ntddcdrm.h
req.target-type: Windows
req.target-min-winverclnt: Obsolete, beginning with Windows Vista.
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
-	ntddcdrm.h
api_name:
-	IOCTL_CDROM_STOP_AUDIO
product:
- Windows
targetos: Windows
req.typenames: 
---

# IOCTL_CDROM_STOP_AUDIO IOCTL


## -description


Ends audio play.  Obsolete, beginning with Windows Vista.


## -ioctlparameters




### -input-buffer

None.


### -input-buffer-length

None.


### -output-buffer

None.


### -output-buffer-length

None.


### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block

The <b>Information</b> field is set to zero. The <b>Status</b> field is set to STATUS_SUCCESS, or possibly to STATUS_INVALID_DEVICE_REQUEST if audio is not currently playing, STATUS_IO_DEVICE_ERROR, STATUS_NO_MEDIA_IN_DEVICE, STATUS_DEVICE_NOT_READY, STATUS_IO_TIME_OUT, or STATUS_VERIFY_REQUIRED.


## -remarks



Beginning with Windows Vista, CDROM class drivers do not use this IOCTL. Prior to Windows Vista, this IOCTL was used for audio playback on older CD-ROM drives that supported direct audio output in hardware.

Client applications should use the <i>Media Control Interface (MCI) API</i> rather than issuing this IOCTL.



