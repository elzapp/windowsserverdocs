---
title: Using the add-DriverPackage Command
description: "Windows Commands topic for **** - "
ms.custom: na
ms.prod: windows-server-threshold
ms.reviewer: na
ms.suite: na
ms.technology: manage-windows-commands
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3ac9e8d5-63ec-4ce8-86fc-85d28011050b
author: coreyp-at-msft
ms.author: coreyp
manager: dongill
ms.date: 10/12/2016
---
# Using the add-DriverPackage Command

>Applies To: Windows Server&reg; 2016, Windows Server&reg; 2012 R2, Windows Server&reg; 2012

adds a driver package to the server.  
  
## Syntax  
  
```  
wdsutil /add-DriverPackage /InfFile:<Inf File path> [/Server:<Server name>] [/Architecture:{x86 | ia64 | x64}] [/DriverGroup:<Group Name>] [/Name:<Friendly Name>]  
```  
  
## Parameters  
  
|Parameter|Description|  
|-------|--------|  
|InfFile:<Inf File path>|Specifies the full path of the .inf file to add.|  
|/Server:<Server name>|Specifies the name of the server. This can be the NetBIOS name or the FQDN. If no server name is specified, the local server is used.|  
|/Architecture:{x86 &#124; ia64 &#124; x64}|Specifies the architecture of the driver package.|  
|[/DriverGroup:<Group Name>]|Specifies the name of the driver group to which the package should be added.|  
|[/Name:<Friendly Name>]|States the friendly name for the driver package.|  
  
## <a name="BKMK_examples"></a>Examples  
To add a driver package, type one of the following:  
  
```  
wdsutil /verbose /add-DriverPackage /InfFile:"C:\Temp\Display.inf"  
```  
  
```  
wdsutil /add-DriverPackage /Server:MyWDSServer /InfFile:"C:\Temp\Display.inf" /Architecture:x86 /DriverGroup:x86Drivers /Name:"Display Driver  
```  
  
#### additional references  
[Command-Line Syntax Key](command-line-syntax-key.md)  
  
[Using the add-AllDriverPackages subcommand]()  
  
