﻿---
title: ADCPROP_UPDATERESYNC_ENUM
TOCTitle: ADCPROP_UPDATERESYNC_ENUM
ms:assetid: 890210c4-2290-ddb2-8814-022093c318de
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249600(v=office.15)
ms:contentKeyID: 48546145
ms.date: 09/18/2015
mtps_version: v=office.15
---

# ADCPROP\_UPDATERESYNC\_ENUM

**Applies to**: Access 2013 | Office 2013

Specifies whether the [UpdateBatch](updatebatch-method-ado.md) method is followed by an implicit [Resync](resync-method-ado.md) method operation and if so, the scope of that operation.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
<th><p>Value</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adResyncAll</strong></p></td>
<td><p>15</p></td>
<td><p>Invokes <strong>Resync</strong> with the combined value of all the other ADCPROP_UPDATERESYNC_ENUM members.</p></td>
</tr>
<tr class="even">
<td><p><strong>adResyncAutoIncrement</strong></p></td>
<td><p>1</p></td>
<td><p>Default. Attempts to retrieve the new identity value for columns that are automatically incremented or generated by the data source, such as Microsoft Jet AutoNumber fields or Microsoft SQL Server Identity columns.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adResyncConflicts</strong></p></td>
<td><p>2</p></td>
<td><p>Invokes <strong>Resync</strong> for all rows in which the update or delete operation failed because of a concurrency conflict.</p></td>
</tr>
<tr class="even">
<td><p><strong>adResyncInserts</strong></p></td>
<td><p>8</p></td>
<td><p>Invokes <strong>Resync</strong> for all successfully inserted rows. However, AutoIncrement column values are not resynchronized. Instead, the contents of newly inserted rows are resynchronized based on the existing primary key value. If the primary key is an AutoIncrement value, <strong>Resync</strong> won't retrieve the contents of the intended row. For automatically incrementing AutoIncrement primary key values, call <strong>UpdateBatch</strong> with the combined value <strong>adResyncAutoIncrement</strong> + <strong>adResyncInserts</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adResyncNone</strong></p></td>
<td><p>0</p></td>
<td><p>Does not invoke <strong>Resync</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adResyncUpdates</strong></p></td>
<td><p>4</p></td>
<td><p>Invokes <strong>Resync</strong> for all successfully updated rows.</p></td>
</tr>
</tbody>
</table>
