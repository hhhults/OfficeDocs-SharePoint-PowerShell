---
external help file: microsoft.office.project.server.stsadmcommandhandler.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/set-spprojectdatabasequota

title: Set-SPProjectDatabaseQuota
schema: 2.0.0
---

# Set-SPProjectDatabaseQuota

## SYNOPSIS
Microsoft internal use only.

## SYNTAX

### settings
```
Set-SPProjectDatabaseQuota [-Settings] <ProjectDatabaseQuotaSettings> -Url <Uri>
 [-AssignmentCollection <SPAssignmentCollection>] [<CommonParameters>]
```

### options
```
Set-SPProjectDatabaseQuota [-Enabled] -MaxDbSize <Int32> -ReadOnlyLimit <Int32>
 -ReadOnlyWarningThreshold <Int32> -Url <Uri> [-AssignmentCollection <SPAssignmentCollection>]
 [<CommonParameters>]
```

## DESCRIPTION
Microsoft internal use only.

For permissions and the most current information about Windows PowerShell for Project Server, see the online documentation at https://go.microsoft.com/fwlink/p/?LinkId=251833 (https://go.microsoft.com/fwlink/p/?LinkId=251833).

## EXAMPLES

### EXAMPLE
```powershell
 {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -Settings

> Applicable: SharePoint Server Subscription Edition

Microsoft internal use only.

```yaml
Type: ProjectDatabaseQuotaSettings
Parameter Sets: settings
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Enabled

> Applicable: SharePoint Server Subscription Edition

Microsoft internal use only.

```yaml
Type: SwitchParameter
Parameter Sets: options
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxDbSize

> Applicable: SharePoint Server Subscription Edition

Microsoft internal use only.

```yaml
Type: Int32
Parameter Sets: options
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReadOnlyLimit

> Applicable: SharePoint Server Subscription Edition

Microsoft internal use only.

```yaml
Type: Int32
Parameter Sets: options
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReadOnlyWarningThreshold

> Applicable: SharePoint Server Subscription Edition

Microsoft internal use only.

```yaml
Type: Int32
Parameter Sets: options
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Url

> Applicable: SharePoint Server Subscription Edition

Microsoft internal use only.

```yaml
Type: Uri
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

Microsoft internal use only.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
