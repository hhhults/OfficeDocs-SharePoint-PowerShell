---
external help file: Microsoft.Office.Server.Search.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/set-spenterprisesearchlinksdatabase
applicable: SharePoint Server Subscription Edition
title: Set-SPEnterpriseSearchLinksDatabase
schema: 2.0.0
---

# Set-SPEnterpriseSearchLinksDatabase

## SYNOPSIS
Sets properties of a links database for a search service application.

## SYNTAX

```
Set-SPEnterpriseSearchLinksDatabase [-Identity] <LinksStorePipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] [-DatabaseName <String>]
 [-DatabasePassword <SecureString>] [-DatabaseServer <String>] [-DatabaseUsername <String>]
 [-FailoverDatabaseServer <String>] [-SearchApplication <SearchServiceApplicationPipeBind>] [-WhatIf]
 [<CommonParameters>]
```

## DESCRIPTION
The `Set-SPEnterpriseSearchLinksDatabase` cmdlet sets properties of a specified links database for a search service application.
A links database stores query logging and analytics information.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
$ssa = Get-SPEnterpriseSearchServiceApplication mySearchServiceApp
Set-SPEnterpriseSearchLinksDatabase -Identity SearchApp_LinksStore -SearchApplication $ssa -FailoverDatabaseServer \\failoverServer
```

This example sets the failover database server to \\\\failoverServer for the links database SearchApp_LinksStore in the search service application mySearchServiceApp.

## PARAMETERS

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies the links database to modify.
The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a LinksStore object, in the form LinksStore1; or an instance of a valid LinksStore object.

```yaml
Type: LinksStorePipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -AssignmentCollection

> Applicable: SharePoint Server Subscription Edition

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

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Confirm

> Applicable: SharePoint Server Subscription Edition

Prompts you for confirmation before executing the command.
For more information, type the following command: `get-help about_commonparameters`

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

### -DatabaseName

> Applicable: SharePoint Server Subscription Edition

Specifies the links database name.

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

### -DatabasePassword

> Applicable: SharePoint Server Subscription Edition

Specifies the password of the account to connect to the database.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseServer

> Applicable: SharePoint Server Subscription Edition

Specifies the server to use for the host SQL database.

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

### -DatabaseUsername

> Applicable: SharePoint Server Subscription Edition

Specifies the name of the account to connect to the database.

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

### -FailoverDatabaseServer

> Applicable: SharePoint Server Subscription Edition

Specifies the server to use for failover when using SQL Server mirroring.

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

### -SearchApplication

> Applicable: SharePoint Server Subscription Edition

Specifies the search application that contains the links database.
The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid SearchServiceApplication object.

```yaml
Type: SearchServiceApplicationPipeBind
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[New-SPEnterpriseSearchLinksDatabase](New-SPEnterpriseSearchLinksDatabase.md)

[Get-SPEnterpriseSearchLinksDatabase](Get-SPEnterpriseSearchLinksDatabase.md)

[Remove-SPEnterpriseSearchLinksDatabase](Remove-SPEnterpriseSearchLinksDatabase.md)

[Move-SPEnterpriseSearchLinksDatabases](Move-SPEnterpriseSearchLinksDatabases.md)
