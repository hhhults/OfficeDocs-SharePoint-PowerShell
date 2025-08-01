---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/new-spwebapplicationappdomain
applicable: SharePoint Server Subscription Edition
title: New-SPWebApplicationAppDomain
schema: 2.0.0
---

# New-SPWebApplicationAppDomain

## SYNOPSIS

Creates an AppDomain entry.

## SYNTAX

```
New-SPWebApplicationAppDomain [-AppDomain] <String> -WebApplication <SPWebApplicationPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] [-Port <Int32>] [-SecureSocketsLayer] [-WhatIf]
 [-Zone <SPUrlZone>] [<CommonParameters>]
```

## DESCRIPTION

Use the New-SPWebApplicationAppDomain cmdlet to create an AppDomain entry. If you specify a port, the cmdlet adds a port binding to the Internet Information Services (IIS) site corresponding to the Web Application/Zone combination.

## EXAMPLES

### EXAMPLE 1

```powershell
New-SPWebApplicationAppDomain -AppDomain contosoapps.com -WebApplication https://www.contoso.com
```

Creates a new app domain for apps for SharePoint for the specified web application in the default zone.

### EXAMPLE 2

```powershell
New-SPWebApplicationAppDomain -AppDomain contosoapps.com -WebApplication https://www.contoso.com -Zone Internet -Port 10000
```

Creates a new app domain for apps for SharePoint for the specified web application in the internet zone at port 10000.

## PARAMETERS

### -AppDomain

> Applicable: SharePoint Server Subscription Edition

Specifies the URI of the app domain.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WebApplication

> Applicable: SharePoint Server Subscription Edition

Specifies the GUID, URI, or name of the web application for which the app domain is being configured.

```yaml
Type: SPWebApplicationPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AssignmentCollection

> Applicable: SharePoint Server Subscription Edition

Manages objects for the purpose of proper disposal. Use of objects, such as SPWeb or SPSite, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the SPAssignment object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When SPWeb, SPSite, or SPSiteAdministration objects are used, the objects are automatically disposed of if an assignment collection or the Global parameter is not used.

When the Global parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the Stop-SPAssignment command, an out-of-memory scenario can occur.

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

### -Port

> Applicable: SharePoint Server Subscription Edition

Specifies the IIS port number to which the app domain will be assigned. If no value is specified, the same port used by the web application for the zone is applied.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SecureSocketsLayer

> Applicable: SharePoint Server Subscription Edition

Specifies that the app domain will use Secured Sockets Layer (SSL) security. If no value is specified, no SSL security will be used.

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

### -Zone

> Applicable: SharePoint Server Subscription Edition

Specifies the security zone to which the app domain will be assigned.

* Default

* Intranet

* Internet

* Extranet

* Custom

If no value is specified, Default is applied.

```yaml
Type: SPUrlZone
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String

Microsoft.SharePoint.PowerShell.SPAssignmentCollection

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Get-SPWebApplicationAppDomain](Get-SPWebApplicationAppDomain.md)

[Remove-SPWebApplicationAppDomain](Remove-SPWebApplicationAppDomain.md)
