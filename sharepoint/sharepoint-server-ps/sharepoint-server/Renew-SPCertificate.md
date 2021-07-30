---
external help file: Microsoft.SharePoint.PowerShell.dll-Help.xml
module name: SharePointServer
online version: https://docs.microsoft.com/powershell/module/sharepoint-server/renew-spcertificate
applicable: SharePoint Server Subscription Edition
title: Renew-SPCertificate
schema: 2.0.0
author:
ms.author:
ms.reviewer:
---

# Renew-SPCertificate

## SYNOPSIS
Renews a certificate and creates a new certificate signing request.

## SYNTAX

### Default (Default)
```powershell
PS C:\> Renew-SPCertificate [-Identity] <SPServerCertificatePipeBind> -FriendlyName <String> [-CommonName <String>]
 [-AlternativeNames <String[]>] [-OrganizationalUnit <String>] [-Organization <String>] [-Locality <String>]
 [-State <String>] [-Country <String>] [-Exportable] [-HashAlgorithm <String>] [-Path <String>] [-Force]
 [-AssignmentCollection <SPAssignmentCollection>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RSA
```powershell
PS C:\> Renew-SPCertificate [-Identity] <SPServerCertificatePipeBind> -FriendlyName <String> [-CommonName <String>]
 [-AlternativeNames <String[]>] [-OrganizationalUnit <String>] [-Organization <String>] [-Locality <String>]
 [-State <String>] [-Country <String>] [-Exportable] [-KeySize <Int32>] [-HashAlgorithm <String>]
 [-Path <String>] [-Force] [-AssignmentCollection <SPAssignmentCollection>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ECC
```powershell
PS C:\> Renew-SPCertificate [-Identity] <SPServerCertificatePipeBind> -FriendlyName <String> [-CommonName <String>]
 [-AlternativeNames <String[]>] [-OrganizationalUnit <String>] [-Organization <String>] [-Locality <String>]
 [-State <String>] [-Country <String>] [-Exportable] [-EllipticCurve <EllipticCurveType>]
 [-HashAlgorithm <String>] [-Path <String>] [-Force] [-AssignmentCollection <SPAssignmentCollection>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
SharePoint supports renewing SSL certificates via the Renew-SPCertificate PowerShell cmdlet.
This creates a new certificate signing request based on the properties of an existing certificate and is the first step in a three-step process to renew an SSL certificate.

Once an SSL certificate request is created via the operation, the SharePoint administrator must submit the certificate request to their SSL certificate authority.
The SSL certificate authority will then generate a signed certificate based on the request and return it to the SharePoint administrator.
The SharePoint administrator must then import the certificate provided by the SSL certificate authority into SharePoint.
SharePoint will then pair the imported certificate with the private key generated by the certificate request operation.
The certificate is then ready to be used by SharePoint.

When you import a certificate as part of a certificate renewal operation, you can specify the Replace switch parameter with the Import-SPCertificate cmdlet.
This tells SharePoint to automatically replace the certificate assignments of the certificate being renewed with the new certificate.

## EXAMPLES

### ------------EXAMPLE-----------
```powershell
PS C:\> Renew-SPCertificate -Identity "Sites Certificate (2020)" -FriendlyName "Sites Certificate (2021)" -Exportable -Path "\\server\fileshare\Team Sites Certificate Signing Request.txt"
```

This example renews a certificate and creates a certificate signing request.

## PARAMETERS

### -AlternativeNames
Additional DNS domain names or IP addresses that this certificate will be assigned to.
Fully Qualified Domain Names (FQDNs) are recommended.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
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

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -CommonName
The primary DNS domain name or IP address that this certificate will be assigned to.
Fully Qualified Domain Names (FQDNs) are recommended.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Country
The 2 letter country code where your organization is legally located.
This must be an ISO 3166-1 alpha-2 country code.
If this parameter is not specified, the default country of the farm will be used.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EllipticCurve
Specifies to use the elliptic curve cryptography key algorithm for your certificate, and the elliptic curve of your public and private ECC keys.

Larger elliptic curves provide more cryptographic strength than smaller elliptic curves, but they're also more computationally expensive and take more time to complete the SSL/TLS connection.
Select nistP256 if you're unsure which elliptic curve to use.
Elliptic curves larger than nistP384 are not recommended.

If neither this parameter nor the KeySize parameter is specified, the default key algorithm and key size / elliptic curve of the farm will be used.

```yaml
Type: EllipticCurveType
Parameter Sets: ECC
Aliases:
Accepted values: Default, nistP256, nistP384, nistP521

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Exportable
Specifies whether the private key of the certificate may be exported.
If this parameter isn't specified, the private key of certificate deployed to the Windows Certificate Store on each server in the SharePoint farm will not be exportable, and SharePoint will not allow you to export the private key from within the SharePoint administration interface.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Specifies to overwrite a file if it already exists at the specified path.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FriendlyName
The friendly name for the certificate.
This name can be used to help you remember the purpose of this certificate.
The friendly name will only be visible to SharePoint farm administrators, not to end users.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HashAlgorithm
Specifies the hash algorithm of your certificate signature, which your certificate authority will use to verify that your certificate request hasn't been tampered with.

Larger hash algorithms provide more cryptographic strength than smaller hash algorithms, but they're also more computationally expensive.
Select SHA256 if you're unsure which hash algorithm to use.
Hash algorithms larger than SHA384 are not recommended.

If this parameter is not specified, the default hash algorithm of the farm will be used.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Default, SHA256, SHA384, SHA512

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Identity
The certificate to be renewed.

```yaml
Type: SPServerCertificatePipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeySize
Specifies to use the RSA key algorithm for your certificate, and the size of your public and private RSA keys in bits.

Larger key sizes provide more cryptographic strength than smaller key sizes, but they're also more computationally expensive and take more time to complete the SSL/TLS connection.
Select 2048 if you're unsure which key size to use.
Key sizes larger than 4096 are not recommended.

If neither this parameter nor the EllipticCurve parameter is specified, the default key algorithm and key size / elliptic curve of the farm will be used.

```yaml
Type: Int32
Parameter Sets: RSA
Aliases:
Accepted values: 0, 2048, 4096, 8192, 16384

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Locality
The name of the city or locality where your organization is legally located.
Do not abbreviate the name.
If this parameter is not specified, the default locality of the farm will be used.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Organization
The legally registered name of your organization or company.
If this parameter is not specified, the default organization of the farm will be used.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OrganizationalUnit
The name of your department within your organization or company.
If this parameter is not specified, the default organizational unit of the farm will be used.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
The path to the certificate signing request file that will be generated.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -State
The name of the state or province where your organization is legally located.
Do not abbreviate the name.
If this parameter is not specified, the default state of the farm will be used.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS