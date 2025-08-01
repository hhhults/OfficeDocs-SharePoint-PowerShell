---
external help file: Microsoft.Office.Server.Search.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/new-spenterprisesearchserviceapplication
applicable: SharePoint Server Subscription Edition
title: New-SPEnterpriseSearchServiceApplication
schema: 2.0.0
---

# New-SPEnterpriseSearchServiceApplication

## SYNOPSIS
Adds a search service application to a farm.

## SYNTAX

```
New-SPEnterpriseSearchServiceApplication [[-Name] <String>]
 -ApplicationPool <SPIisWebServiceApplicationPoolPipeBind> [-AssignmentCollection <SPAssignmentCollection>]
 [-Confirm] [-DatabaseName <String>] [-DatabasePassword <SecureString>] [-DatabaseServer <String>]
 [-DatabaseUsername <String>] [-Partitioned] [-WhatIf]
 [-AdminApplicationPool <SPIisWebServiceApplicationPoolPipeBind>] [-CloudIndex <Boolean>]
 [-FailoverDatabaseServer <String>] [<CommonParameters>]
```

## DESCRIPTION
This cmdlet is used when the search functionality is first configured or when a new shared search application is added to a farm.
SPEnterpriseSearchServiceApplication represents a self-contained aggregation of indexed content and properties available for search and provides an anchor class for setting global search properties.
A farm can include multiple search service applications.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
$appPool = New-SPServiceApplicationPool -Name 'SharePoint Web Services Default' -Account 'CONTOSO\ServiceApps'
New-SPEnterpriseSearchServiceApplication -Name "Search Service Application" -ApplicationPool $appPool
```

This example creates a new search service application named NewSSA in a new application pool.

A search service application that is created in this manner will have active search topology, but no search components.

## PARAMETERS

### -Name

> Applicable: SharePoint Server Subscription Edition

Specifies the names of the new search application.

The type must be a valid name of a search application, for example, SearchApp1.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationPool

> Applicable: SharePoint Server Subscription Edition

Specifies the IIS application pool to use for the new search application.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid URL of a search application, in the form https://server_name; or an instance of a valid SPIisWebServiceApplicationPool object.

```yaml
Type: SPIisWebServiceApplicationPoolPipeBind
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

Specifies the name of the database to create for the new search application.

The type must be a valid name of a SQL Server database, for example, SearchAppDB1.

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

Specifies the password for the user ID that is used for accessing the search application database on SQL Server.

The type must be a valid password.

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

Specifies the name of the host server for the database specified in DatabaseName.

The type must be a valid SQL Server host name, for example, SQLServerHost1.

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

Specifies the user ID to use for accessing the search application SQL Server database.

The type must be a valid user name, for example, SearchUserName1.

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

### -Partitioned

> Applicable: SharePoint Server Subscription Edition

Specifies that the search service application uses web-hosted mode.
Web-hosted mode segregates results for a given hosted subscription.

This property has no effect on SharePoint Server 2019.

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

Displays a message that describes the effect of the command instead of executing the command.
For more information, type the following command: `get-help about_commonparameters`

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

### -AdminApplicationPool

> Applicable: SharePoint Server Subscription Edition

Specifies the application pool to be used with the SearchAdminWebServiceApplication that is associated with SearchServiceApplication. If not specified, ApplicationPool will be used.

```yaml
Type: SPIisWebServiceApplicationPoolPipeBind
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CloudIndex

> Applicable: SharePoint Server Subscription Edition

When CloudIndex is true, this becomes a cloud Search service application that crawls on premises content in a cloud hybrid search solution.

```yaml
Type: Boolean
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

Specifies the name of the SQL server that hosts the mirror instances of search databases.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
