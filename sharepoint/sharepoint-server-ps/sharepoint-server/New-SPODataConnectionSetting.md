---
external help file: Microsoft.SharePoint.PowerShell.dll-Help.xml
module name: SharePointServer
online version: https://docs.microsoft.com/powershell/module/sharepoint-server/new-spodataconnectionsetting
applicable: SharePoint Server Subscription Edition
title: New-SPODataConnectionSetting
schema: 2.0.0
author:
ms.author:
ms.reviewer:
---

# New-SPODataConnectionSetting

## SYNOPSIS
{{ Fill in the Synopsis }}

## SYNTAX

```
New-SPODataConnectionSetting -ServiceContext <SPServiceContextPipeBind> -Name <String> -ServiceAddressURL <Uri>
 -AuthenticationMode <ODataAuthenticationMode> [-SecureStoreTargetApplicationId <String>]
 [-ExtensionProvider <String>] [-AssignmentCollection <SPAssignmentCollection>] [<CommonParameters>]
```

## DESCRIPTION
{{ Fill in the Description }}

## EXAMPLES

### -------------EXAMPLE 1------------- 
```powershell
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

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

### -AuthenticationMode
{{ Fill AuthenticationMode Description }}

```yaml
Type: ODataAuthenticationMode
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Server Subscription Edition
Accepted values: PassThrough, RevertToSelf, Credentials, WindowsCredentials, DigestCredentials, ClientCertificate, Anonymous

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExtensionProvider
{{ Fill ExtensionProvider Description }}

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
{{ Fill Name Description }}

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Server Subscription Edition

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SecureStoreTargetApplicationId
{{ Fill SecureStoreTargetApplicationId Description }}

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Server Subscription Edition

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceAddressURL
{{ Fill ServiceAddressURL Description }}

```yaml
Type: Uri
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Server Subscription Edition

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceContext
{{ Fill ServiceContext Description }}

```yaml
Type: SPServiceContextPipeBind
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Server Subscription Edition

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.SharePoint.PowerShell.SPAssignmentCollection

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS