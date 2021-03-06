---
external help file:
applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Online
schema: 2.0.0
author: vesajuvonen
ms.author: vesaj
ms.reviewer:
---
# Remove-PnPListItem

## SYNOPSIS
Deletes an item from a list

## SYNTAX 

```powershell
Remove-PnPListItem -List <ListPipeBind>
                   -Identity <ListItemPipeBind>
                   [-Recycle [<SwitchParameter>]]
                   [-Force [<SwitchParameter>]]
                   [-Web <WebPipeBind>]
                   [-Connection <SPOnlineConnection>]
```

## EXAMPLES

### ------------------EXAMPLE 1------------------
```powershell
Remove-PnPListItem -List "Demo List" -Identity "1" -Force
```

Removes the listitem with id "1" from the "Demo List" list.

### ------------------EXAMPLE 2------------------
```powershell
Remove-PnPListItem -List "Demo List" -Identity "1" -Force -Recycle
```

Removes the listitem with id "1" from the "Demo List" list and saves it in the Recycle Bin.

## PARAMETERS

### -Force
Specifying the Force parameter will skip the confirmation question.

```yaml
Type: SwitchParameter
Parameter Sets: (All)

Required: False
Position: Named
Accept pipeline input: False
```

### -Identity
The ID of the listitem, or actual ListItem object

```yaml
Type: ListItemPipeBind
Parameter Sets: (All)

Required: True
Position: Named
Accept pipeline input: False
```

### -List
The ID, Title or Url of the list.

```yaml
Type: ListPipeBind
Parameter Sets: (All)

Required: True
Position: 0
Accept pipeline input: True
```

### -Recycle


```yaml
Type: SwitchParameter
Parameter Sets: (All)

Required: False
Position: Named
Accept pipeline input: False
```

### -Connection
Optional connection to be used by the cmdlet. Retrieve the value for this parameter by either specifying -ReturnConnection on Connect-PnPOnline or by executing Get-PnPConnection.

```yaml
Type: SPOnlineConnection
Parameter Sets: (All)

Required: False
Position: Named
Accept pipeline input: False
```

### -Web
This parameter allows you to optionally apply the cmdlet action to a subweb within the current web. In most situations this parameter is not required and you can connect to the subweb using Connect-PnPOnline instead. Specify the GUID, server relative url (i.e. /sites/team1) or web instance of the web to apply the command to. Omit this parameter to use the current web.

```yaml
Type: WebPipeBind
Parameter Sets: (All)

Required: False
Position: Named
Accept pipeline input: False
```

## RELATED LINKS

[SharePoint Developer Patterns and Practices](http://aka.ms/sppnp)
