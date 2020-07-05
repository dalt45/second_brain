# [[Voice control attributes]]

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribute</th>
<th>Type</th>
<th>Description</th>
<th>Sample manifest entry</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><code>supports_etc_seek</code></td>
<td>integer</td>
<td>Enables handling of "seek" and "start over" voice commands.<br />
<br />
If this flag is not enabled, an error message is displayed when a channel receives a "seek" or "start over" command.</td>
<td><code>supports_etc_seek=1</code></td>
</tr>
<tr class="even">
<td><code>supports_etc_next</code></td>
<td>integer</td>
<td>Enables handling of "next" voice commands.<br />
<br />
If this flag is not enabled, an error message is displayed when a channel receives a "next" command.</td>
<td><code>supports_etc_next=1</code></td>
</tr>
</tbody>
</table>