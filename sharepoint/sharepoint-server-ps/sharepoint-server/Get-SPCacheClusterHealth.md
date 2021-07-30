---
external help file: Microsoft.SharePoint.PowerShell.dll-Help.xml
module name: SharePointServer
online version: https://docs.microsoft.com/powershell/module/sharepoint-server/get-spcacheclusterhealth
applicable: SharePoint Server Subscription Edition
title: Get-SPCacheClusterHealth
schema: 2.0.0
author:
ms.author:
ms.reviewer:
---

# Get-SPCacheClusterHealth

## SYNOPSIS
Returns health statistics for all of the named caches in the cache cluster.
This includes those that haven't been allocated yet.

## SYNTAX

```
Get-SPCacheClusterHealth [-AssignmentCollection <SPAssignmentCollection>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
Use the Get-SPCacheClusterHealth cmdlet to Returns get statistics for all of the named caches in the cache cluster.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at https://go.microsoft.com/fwlink/p/?LinkId=251831 (https://go.microsoft.com/fwlink/p/?LinkId=251831).

## EXAMPLES

### -------------EXAMPLE------------- 
```powershell
PS C:\> Get-SPCacheClusterHealth
```

This example returns health statistics for all of the named caches in the cache cluster.

## PARAMETERS

### -AssignmentCollection
Manages objects for the purpose of proper disposal.
Use of objects, such as SPWeb or SPSite, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management.
Using the SPAssignment object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory.
When SPWeb, SPSite, or SPSiteAdministration objects are used, the objects are automatically disposed of if an assignment collection or the Global parameter is not used.

When the Global parameter is used, all objects are contained in the global store.
If objects are not immediately used, or disposed of by using the Stop-SPAssignment command, an out-of-memory scenario can occur.

```yaml
Type: SPAssignmentCollection
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Displays a message that describes the effect of the command instead of executing the command.
For more information, type the following command: \`get-help about_commonparameters\`

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS