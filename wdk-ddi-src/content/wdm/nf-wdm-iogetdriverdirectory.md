---
UID: NF:wdm.IoGetDriverDirectory
title: IoGetDriverDirectory function
author: windows-driver-content
description: TBD
ms.assetid: ff2a6c2a-e402-4e8a-920a-c9baa9aa237e
ms.author: windowsdriverdev
ms.date: 
ms.topic: function
ms.keywords: IoGetDriverDirectory
req.header: wdm.h
req.include-header:
req.target-type:
req.target-min-winverclnt: 
req.target-min-winversvr:
req.kmdf-ver:
req.umdf-ver:
req.lib: NtosKrnl.lib
req.dll: NtosKrnl.exe
req.irql: PASSIVE_LEVEL
req.ddi-compliance:
req.unicode-ansi:
req.idl:
req.max-support:
req.namespace:
req.assembly:
req.type-library: 
topictype: 
-	apiref
apitype: 
-	DllExport
apilocation: 
-	NtosKrnl.exe
apiname: 
-	IoGetDriverDirectory
product: Windows
targetos: Windows

---

# IoGetDriverDirectory function


## -description

Returns a handle to a directory on disk from which the driver can read and write files. The files in that directory apply to a specific driver object.

## -parameters

### -param DriverObject
[_In_] A pointer to the driver object ([**DRIVER_OBJECT**](ns-wdm-_driver_object.md) structure) of the calling driver.

### -param DirectoryType
[_In_] A [**_DRIVER_DIRECTORY_TYPE**](ne-wdm-_driver_directory_type.md)-type value that indicates the type of requested directory.

### -param Flags
[_In_] Must be 0.

### -param DriverDirectoryHandle
[_Out_] A pointer to a variable that receives a HANDLE to the requested driver directory. The caller must not pass NULL.

## -returns

Returns an appropriate [NTSTATUS value](https://docs.microsoft.com/en-us/windows-hardware/drivers/kernel/ntstatus-values). Possible values include:
| Error code               | Description                                                                                        |
| ------------------------ | -------------------------------------------------------------------------------------------------- |
| STATUS_SUCCESS           | The call successfully opened a handle to the requested driver directory.                           |
| STATUS_INVALID_PARAMETER | An input value to this function is invalid. For example, _DriverObject_ or _DriverDirectoryHandle_ is NULL;  _Flags_ is not 0. |

## -remarks
If **IoGetDriverDirectory** is called before the required disks and volumes have been started, the function does not open a handle and returns an error. 

The driver must call [**ZwClose**](..\ntifs\nf-ntifs-ntclose.md) to close the received handle when access is no longer required.

Callers of **IoGetDriverDirectory** must be running at IRQL = PASSIVE_LEVEL in the context of a system thread.


## -see-also
[**DRIVER_OBJECT**](ns-wdm-_driver_object.md) 

[**_DRIVER_DIRECTORY_TYPE**](ne-wdm-_driver_directory_type.md)

[**ZwClose**](..\ntifs\nf-ntifs-ntclose.md)
