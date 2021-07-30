---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
module name: Microsoft.SharePoint.Powershell
online version: https://docs.microsoft.com/powershell/module/sharepoint-server/remove-sproutingmachineinfo
applicable: SharePoint Server Subscription Edition
title: Remove-SPRoutingMachineInfo
schema: 2.0.0
author: techwriter40
ms.author: pamgreen
ms.reviewer: 
---

# Remove-SPRoutingMachineInfo

## SYNOPSIS
Removes an external routing target.


## SYNTAX

```
Remove-SPRoutingMachineInfo [-Identity] <SPRoutingMachineInfoPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [<CommonParameters>]
```

## DESCRIPTION
Use the `Remove-SPRoutingMachineInfo` cmdlet to remove an external routing target by using the Identity parameter.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://docs.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).


## EXAMPLES

### ----------EXAMPLE-------
```powershell
PS C:\> $web=Get-SPWebApplication -Identity <URL of web application>

PS C:\> $rm=Get-SPRequestManagementSettings -Identity $web

PS C:\> $M=Get-SPRoutingMachineInfo -RequestManagementSettings $rm -Name <MachineName>

Remove-SPRoutingMachineInfo -Identity $M
```

This example removes a routing target for a specified identity.


## PARAMETERS

### -Identity
Specifies the computer object that Request Manager will remove.

```yaml
Type: SPRoutingMachineInfoPipeBind
Parameter Sets: (All)
Aliases: 
Applicable: SharePoint Server Subscription Edition

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -AssignmentCollection
Manages objects for the purpose of proper disposal.
Use of objects, such as SPWeb or SPSite, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management.
Using the SPAssignment object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory.
When SPWeb, SPSite, or SPSiteAdministration objects are used, the objects are automatically disposed of if an assignment collection or the Global parameter is not used.

When the Global parameter is used, all objects are contained in the global store.
If objects are not immediately used, or disposed of by using the `Stop-SPAssignment` command, an out-of-memory scenario can occur.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Add-SPRoutingMachineInfo](Add-SPRoutingMachineInfo.md)

[Get-SPRoutingMachineInfo](Get-SPRoutingMachineInfo.md)

[Set-SPRoutingMachineInfo](Set-SPRoutingMachineInfo.md)