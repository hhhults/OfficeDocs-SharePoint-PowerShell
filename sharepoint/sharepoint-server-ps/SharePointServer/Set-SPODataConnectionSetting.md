---
external help file: Microsoft.SharePoint.PowerShell.dll-Help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/set-spodataconnectionsetting
applicable: SharePoint Server Subscription Edition
title: Set-SPODataConnectionSetting
schema: 2.0.0
---

# Set-SPODataConnectionSetting

## SYNOPSIS
{{ Fill in the Synopsis }}

## SYNTAX

### Name (Default)
```
Set-SPODataConnectionSetting -ServiceContext <SPServiceContextPipeBind> -Name <String>
 [-ServiceAddressURL <Uri>] [-AuthenticationMode <ODataAuthenticationMode>]
 [-SecureStoreTargetApplicationId <String>] [-ExtensionProvider <String>]
 [-AssignmentCollection <SPAssignmentCollection>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Identity
```
Set-SPODataConnectionSetting -ServiceContext <SPServiceContextPipeBind> [-ServiceAddressURL <Uri>]
 [-AuthenticationMode <ODataAuthenticationMode>] [-SecureStoreTargetApplicationId <String>]
 [-ExtensionProvider <String>] [-Identity] <ODataConnectionSettings>
 [-AssignmentCollection <SPAssignmentCollection>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
{{ Fill in the Description }}

## EXAMPLES

### EXAMPLE 1
```powershell
{{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -AssignmentCollection

> Applicable: SharePoint Server Subscription Edition

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

### -AuthenticationMode

> Applicable: SharePoint Server Subscription Edition

{{ Fill AuthenticationMode Description }}

```yaml
Type: ODataAuthenticationMode
Parameter Sets: (All)
Aliases:

Accepted values: PassThrough, RevertToSelf, Credentials, WindowsCredentials, DigestCredentials, ClientCertificate, Anonymous

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExtensionProvider

> Applicable: SharePoint Server Subscription Edition

{{ Fill ExtensionProvider Description }}

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

### -Identity

> Applicable: SharePoint Server Subscription Edition

{{ Fill Identity Description }}

```yaml
Type: ODataConnectionSettings
Parameter Sets: Identity
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

> Applicable: SharePoint Server Subscription Edition

{{ Fill Name Description }}

```yaml
Type: String
Parameter Sets: Name
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SecureStoreTargetApplicationId

> Applicable: SharePoint Server Subscription Edition

{{ Fill SecureStoreTargetApplicationId Description }}

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

### -ServiceAddressURL

> Applicable: SharePoint Server Subscription Edition

{{ Fill ServiceAddressURL Description }}

```yaml
Type: Uri
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceContext

> Applicable: SharePoint Server Subscription Edition

{{ Fill ServiceContext Description }}

```yaml
Type: SPServiceContextPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm

> Applicable: SharePoint Server Subscription Edition

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

> Applicable: SharePoint Server Subscription Edition

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.SharePoint.BusinessData.SystemSpecific.OData.ODataConnectionSettings

### Microsoft.SharePoint.PowerShell.SPAssignmentCollection

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
