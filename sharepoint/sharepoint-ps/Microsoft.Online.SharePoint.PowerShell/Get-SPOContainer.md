---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spocontainer
applicable: SharePoint Online
title: Get-SPOContainer
schema: 2.0.0
author: ShreyasSar26
ms.author: shsaravanan
ms.reviewer:
---

# Get-SPOContainer

## SYNOPSIS

Returns one or more containers in a SharePoint Embedded application.

## SYNTAX

### OwningApplicationId
```
Get-SPOContainer [-OwningApplicationId] <Guid> [-Paged] [[-PagingToken] <String>] [<CommonParameters>]
```

### Sort
```
Get-SPOContainer [-OwningApplicationId] <Guid> [-Paged] [[-PagingToken] <String>] [-SortByStorage] <SortOrder>
 [<CommonParameters>]
```

### Archive
```
Get-SPOContainer [-OwningApplicationId] <Guid> [-Paged] [[-PagingToken] <String>]
 [[-SortByStorage] <SortOrder>] [-ArchiveStatus] <SPContainerArchiveStatusFilterProperties>
 [<CommonParameters>]
```

### Identity
```
Get-SPOContainer -Identity <SPOContainerPipeBind> [<CommonParameters>]
```

## DESCRIPTION

The `Get-SPOContainer` cmdlet retrieves details of an individual container, either in the active or archived state, when paired with the `Identity` parameter, which requires specifying the container ID. When used with the `OwningApplicationId` parameter, the cmdlet returns a list of active containers associated with a SharePoint Embedded application. Additionally, when also used with the `ArchiveStatus` parameter, it returns a list of containers in the archived state as specified.

You must be a SharePoint Embedded Administrator to run this cmdlet.

For permissions and the most current information about Windows PowerShell for SharePoint Embedded Containers, see the documentation at [Intro to SharePoint Embedded Containers Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

> [!NOTE]
> Containers in the Recycle Bin will not be retrieved by using the `Get-SPOContainer` cmdlet.
> The OwningApplicationId for Microsoft Loop is `a187e399-0c36-4b98-8f04-1edc167a0996`.
> The OwningApplicationId for Microsoft Designer is `5e2795e3-ce8c-4cfb-b302-35fe5cd01597`.

## EXAMPLES

### Example 1

```powershell
Get-SPOContainer -Identity b66f5b2e
```

Example 1 returns the detailed properties of the Container with associated Container ID b66f5b2e.

### Example 2

```powershell
Get-SPOContainer -OwningApplicationId 423poi45 | ft
```
Example 2 returns a tabular list of Containers created under the SharePoint Embedded application with the `OwningApplicationId` of  `423poi45`.

### Example 3

```powershell
Get-SPOContainer -OwningApplicationId 423poi45 -Paged | ft
```
Example 3 uses the `-Paged` command to retrieve a paging token.

### Example 4

```powershell
Get-SPOContainer -OwningApplicationId 423poi45 -Paged -PagingToken <zacad> | ft
```

Example 4 uses the `-PagingToken` parameter along with the `-Paged` parameter to view more containers that were not displayed in Example 3.

### Example 5

```powershell
Get-SPOContainer -OwningApplicationId 423poi45 -SortByStorage Ascending
```

Example 5 displays the containers belonging to the application, sorted in ascending order of storage.

### Example 6

```powershell
Get-SPOContainer -OwningApplicationId 423poi45 -SortByStorage Ascending -Paged
```

Example 6 displays a paged view of the the containers belonging to the application, sorted in ascending order of storage.

### Example 7

```powershell
Get-SPOContainer -OwningApplicationId 423poi45-as -SortByStorage Ascending -Paged -PagingToken <zacad>
```

Example 7 displays the next list of paged view of containers belonging to the application, sorted in ascending order of storage.

### Example 8

```powershell
Get-SPOContainer -OwningApplicationId 423poi45 -ArchiveStatus RecentlyArchived | ft
```

Example 8 returns a tabular list of recently archived containers belonging to the SharePoint Embedded application with the OwningApplicationId of 423poi45.

## PARAMETERS

### -ArchiveStatus

> Applicable: SharePoint Online

The ArchiveStatus parameter is used to display containers in various stages of archiving. The following states are supported:

- Archived – Displays containers in all archived states.
- RecentlyArchived – Displays containers in the "Recently archived" state.
- FullyArchived – Displays containers in the "Fully archived" state.
- Reactivating – Displays containers in the "Reactivating" state.
- NotArchived – Displays active containers

```yaml
Type: Microsoft.Online.SharePoint.TenantAdministration.SPContainerArchiveStatusFilterProperties
Parameter Sets: Archive
Aliases:
Accepted values: NotArchived, FullyArchived, RecentlyArchived, Reactivating, Archived

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Identity

> Applicable: SharePoint Online

Use this parameter to specify the Container ID.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SPOContainerPipeBind
Parameter Sets: Identity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OwningApplicationId

> Applicable: SharePoint Online

This parameter specifies the ID of the SharePoint Embedded application. Use the `Get-SPOApplication` command to retrieve the OwningApplicationId.

```yaml
Type: System.Guid
Parameter Sets: OwningApplicationId, Sort, Archive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Paged

> Applicable: SharePoint Online

This parameter can be used when there are more than 200 containers in a given SharePoint Embedded application. Using `-Paged` will provide a paging token that will display the next 200 Containers.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OwningApplicationId, Sort, Archive
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PagingToken

> Applicable: SharePoint Online

Use this parameter to provide the paging token to view the remaining containers as shown in Example 4. If there are no more containers to display, the cmdlet output will return the message `End of containers view.` Otherwise, use the given paging token to retrieve the next batch of up to 200 containers. For displaying the next set of archived containers, `-ArchiveStatus` paramter needs to be used along with this parameter.

```yaml
Type: System.String
Parameter Sets: OwningApplicationId, Sort, Archive
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SortByStorage

This parameter can be used when you need to see the list of containers, sorted by storage.

```yaml
Type: Microsoft.Online.SharePoint.TenantManagement.SortOrder
Parameter Sets: Sort
Aliases:
Accepted values: Ascending, Descending

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Intro to SharePoint Embedded Containers Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell)

[Get-SPOApplication](./Get-SPOApplication.md)

[Set-SPOContainer](./Set-SPOContainer.md)

[Get-SPODeletedContainer](./Get-SPODeletedContainer.md)

[Remove-SPOContainer](./Remove-SPOContainer.md)

[Remove-SPODeletedContainer](./Remove-SPODeletedContainer.md)

[Restore-SPODeletedContainer](./Restore-SPODeletedContainer.md)

