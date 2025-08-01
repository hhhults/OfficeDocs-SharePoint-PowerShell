---
external help file: microsoft.office.access.server.dll-help.xml
Module Name: Microsoft.SharePoint.Powershell
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/new-spaccessservicesapplication
applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019
title: New-SPAccessServicesApplication
schema: 2.0.0
author: techwriter40
ms.author: pamgreen
ms.reviewer:
---

# New-SPAccessServicesApplication

## SYNOPSIS
Creates an Access Services Service Application.

## SYNTAX

### DefaultParameterSet
```
New-SPAccessServicesApplication -ApplicationPool <SPIisWebServiceApplicationPoolPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-CacheTimeout <Int32>] [-Confirm] -DatabaseServer <String>
 [-DatabaseServerCredentials <PSCredential>] [-Default] [-Encrypt <Boolean>] [-Hosted <Boolean>]
 [-Name <String>] [-PrivateBytesMax <Int32>] [-QueryTimeout <Int32>] [-RecoveryPointObjective <Int32>]
 [-RequestDurationMax <Int32>] [-SessionsPerAnonymousUserMax <Int32>] [-SessionsPerUserMax <Int32>]
 [-TrustServerCertificate <Boolean>] [-WhatIf] [<CommonParameters>]
```

### NoApplicationServerParameterSet
```
New-SPAccessServicesApplication -ApplicationPool <SPIisWebServiceApplicationPoolPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-CacheTimeout <Int32>] [-Confirm] [-Default]
 [-Hosted <Boolean>] [-Name <String>] [-PrivateBytesMax <Int32>] [-QueryTimeout <Int32>]
 [-RecoveryPointObjective <Int32>] [-RequestDurationMax <Int32>] [-SessionsPerAnonymousUserMax <Int32>]
 [-SessionsPerUserMax <Int32>] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
Creates an Access Services Service Application.

## EXAMPLES

### Example 1
```
New-SPAccessServicesApplication -DatabaseServer SQLServerName -ApplicationPool 'SharePoint Web Services Default' -Name 'Access Services Service Application' -Default
```

Creates an Access Services Service Application.

## PARAMETERS

### -ApplicationPool

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies the existing IIS application pool in which to run the Web service for the service application.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of an application pool (for example, AppPoolName1); or an instance of a valid IISWebServiceApplicationPool object.

```yaml
Type: SPIisWebServiceApplicationPoolPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -AssignmentCollection

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

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

### -CacheTimeout

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

The maximum time (in seconds) that a data cache can remain available, as measured from the end of each request for data in that cache.

Valid values: -1 (indicates no limit); 1 through 2073600 (24 days).

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

### -Confirm

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

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

### -DatabaseServer

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies the name of the host server for the database specified in DatabaseName.

The type must be a valid SQL Server host name; for example, SERVER\Database.

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseServerCredentials

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies the credentials used to log into the database server.

```yaml
Type: PSCredential
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Default

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Add to default Service Application Proxy group.

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameterSet, NoApplicationServerParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Encrypt

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies to use SSL encryption between Access Services and the SQL Server hosting Access Services databases.

```yaml
Type: Boolean
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Hosted

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Not used.

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

### -Name

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies the name of the Access Services Service Application to create.

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

### -PrivateBytesMax

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

The maximum number of private bytes (in MB) allocated by the Access Services process.

Valid values: -1 (the limit is set to 50% of physical memory on the machine), any positive integer.

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

### -QueryTimeout

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Maximum time in seconds for a database command or query to execute before it is cancelled.

Valid values: 0 (indicates no limit); 1 through 2073600 (24 days). Recommended value is 60.

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

### -RecoveryPointObjective

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Not used.

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

### -RequestDurationMax

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

The maximum duration (in seconds) allowed for a request from an application.

Valid values: -1 (indicates no limit); 1 through 2073600 (24 days).

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

### -SessionsPerAnonymousUserMax

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

The maximum number of sessions allowed per anonymous user. If this maximum is hit the oldest session will be deleted when a new session is started.

Valid values: -1 (no limit), 1 to any positive integer.

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

### -SessionsPerUserMax

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

The maximum number of sessions allowed per user. If a user has this many sessions and starts a new session, the user's oldest session is deleted.

Valid values: -1 (no limit), from 1 to any positive integer.

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

### -TrustServerCertificate

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Sets a value that indicates whether the channel will be encrypted while bypassing walking the certificate chain to validate trust.

```yaml
Type: Boolean
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

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

### Microsoft.SharePoint.PowerShell.SPIisWebServiceApplicationPoolPipeBind
Microsoft.SharePoint.PowerShell.SPAssignmentCollection

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
