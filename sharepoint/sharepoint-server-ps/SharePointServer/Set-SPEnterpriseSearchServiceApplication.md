---
external help file: Microsoft.Office.Server.Search.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/set-spenterprisesearchserviceapplication
applicable: SharePoint Server Subscription Edition
title: Set-SPEnterpriseSearchServiceApplication
schema: 2.0.0
---

# Set-SPEnterpriseSearchServiceApplication

## SYNOPSIS
Sets the properties of a search service application for a farm.

## SYNTAX

```
Set-SPEnterpriseSearchServiceApplication [-AdminApplicationPool <SPIisWebServiceApplicationPoolPipeBind>]
 [-ApplicationPool <SPIisWebServiceApplicationPoolPipeBind>] [-AssignmentCollection <SPAssignmentCollection>]
 [-Confirm] [-DatabaseName <String>] [-DatabasePassword <SecureString>] [-DatabaseServer <String>]
 [-DatabaseUsername <String>] [-DefaultContentAccessAccountName <String>]
 [-DefaultContentAccessAccountPassword <SecureString>] [-DefaultSearchProvider <SearchProvider>]
 [-DiacriticSensitive <String>] [-FailoverDatabaseServer <String>] -Identity <SearchServiceApplicationPipeBind>
 [-VerboseQueryMonitoring <String>] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
This cmdlet updates properties of a search service application.
SPEnterpriseSearchServiceApplication represents a self-contained aggregation of indexed content and properties available for search and provides an anchor class for setting global search properties.
A search application can include multiple search service applications.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
Set-SPEnterpriseSearchServiceApplication -Identity "Search Service Application" -VerboseQueryMonitoring True
```

This example turns on verbose query logging in the default search service application named Search Service Application.

## PARAMETERS

### -AdminApplicationPool

> Applicable: SharePoint Server Subscription Edition

Specifies the application pool for the administrative web service for the search service application.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of an application pool (for example, AdminAppPool1); or an instance of a valid IISWebServiceApplicationPool object.

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

### -ApplicationPool

> Applicable: SharePoint Server Subscription Edition

Specifies an application pool for the search service application.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of an application pool (for example, AppPool1); or an instance of a valid IISWebServiceApplicationPool object.

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

This parameter is obsolete and has no function.
You should not use this parameter.

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

Specifies the password for the user ID that is used for accessing the web service administration database on SQL Server.

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

Specifies the name of the host server for the web service administration database.

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

Specifies the user ID to use for accessing the web service administration database.

The type must be a valid user name, for example, WebAdminUserDB1.

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

### -DefaultContentAccessAccountName

> Applicable: SharePoint Server Subscription Edition

Specifies the account ID to use for accessing content.

The type must be a valid user name, for example, ContentAccessUser1.

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

### -DefaultContentAccessAccountPassword

> Applicable: SharePoint Server Subscription Edition

Specifies the password for the content access account.

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

### -DefaultSearchProvider

> Applicable: SharePoint Server Subscription Edition

Specifies the search application type to be used for this application.
This parameter has been deprecated for SharePoint Server.

```yaml
Type: SearchProvider
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiacriticSensitive

> Applicable: SharePoint Server Subscription Edition

Specifies that the search application respects diacritics (for example, ä).
The default value is false.

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

Specifies the name of the host SQL instance for the failover database server.

The type must be a valid SQL Server instance name, for example, SQLServerHost1.

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

Specifies the search service application to update.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a search service application (for example, MySearchApp); or an instance of a valid SearchServiceApplication object.

```yaml
Type: SearchServiceApplicationPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VerboseQueryMonitoring

> Applicable: SharePoint Server Subscription Edition

Enables verbose query logging.
The default value is False.

The type must be a string that can be cast to a Boolean value, for example, True or False.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
