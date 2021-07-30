---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
module name: Microsoft.SharePoint.Powershell
online version: https://docs.microsoft.com/powershell/module/sharepoint-server/add-sproutingrule
applicable: SharePoint Server Subscription Edition
title: Add-SPRoutingRule
schema: 2.0.0
author: techwriter40
ms.author: pamgreen
ms.reviewer:
---

# Add-SPRoutingRule

## SYNOPSIS

Adds a routing rule.



## SYNTAX

```
Add-SPRoutingRule [-RequestManagementSettings] <SPRequestManagementSettingsPipeBind> [-Name] <String>
 [-AssignmentCollection <SPAssignmentCollection>] [-Criteria <SPRequestManagementRuleCriteriaPipeBind[]>]
 [-ExecutionGroup <Int32>] [-Expiration <DateTime>] [-MachinePool <SPRoutingMachinePoolPipeBind>]
 [<CommonParameters>]
```

## DESCRIPTION
The Add-SPRoutingRule cmdlet adds a routing rule for the farm.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://docs.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### --------------EXAMPLE-------- 
```powershell
PS C:\> $rm=Get-SPRequestManagementSettings -Identity $web

PS C:\> Get-SPRoutingRule -RequestManagementSettings $rm

PS C:\> $machines=Get-SPRoutingMachineInfo -RequestManagementSettings $rm

PS C:\> Add-SPRoutingMachinePool -RequestManagementSettings $rm -Name <Name of Pool> -MachineTargets $machines
```

This examples adds a routing rule to the farm by using the $rm and $machines variables.

## PARAMETERS

### -RequestManagementSettings
Specifies the name of the request management settings object to add to the routing rule.

```yaml
Type: SPRequestManagementSettingsPipeBind
Parameter Sets: (All)
Aliases: 
Applicable: SharePoint Server Subscription Edition

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies the name of the rule.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Applicable: SharePoint Server Subscription Edition

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -Criteria
Specifies the criteria for the rule to match.

```yaml
Type: SPRequestManagementRuleCriteriaPipeBind[]
Parameter Sets: (All)
Aliases: 
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExecutionGroup
Specifies the group in which the rule will be placed.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Expiration
Specifies the expiration date and time of the rule.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MachinePool
Specifies the pool of machines to which a request will be routed if the created rule is matched.

```yaml
Type: SPRoutingMachinePoolPipeBind
Parameter Sets: (All)
Aliases: 
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-SPRoutingRule](Get-SPRoutingRule.md)

[Remove-SPRoutingRule](Remove-SPRoutingRule.md)

[Set-SPRoutingRule](Set-SPRoutingRule.md)
