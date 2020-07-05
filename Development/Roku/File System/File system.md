## Application Storage

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Storage</th>
<th>Advantages</th>
<th>Disadvantages</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>file in tmp:</td>
<td>Files are read/write</td>
<td>Contents are not retained when application exits</td>
</tr>
<tr class="even">
<td>file in cachefs:</td>
<td>Files are read/write; an arbitrary amount of data can be written.<br />
<br />
cachefs use is per developer ID. Files in cachefs are stored in RAM; therefore, a reboot will evict them from cachefs.</td>
<td>Data is evicted when more space is required for another Channel</td>
</tr>
<tr class="odd">
<td>file in pkg:</td>
<td>Accesses any files included in app package</td>
<td>Files are read-only</td>
</tr>
<tr class="even">
<td>file on USB device</td>
<td>Accesses files on removable USB media</td>
<td>Files are read-only; not all Roku models support USB</td>
</tr>
<tr class="odd">
<td>Registry</td>
<td>Data is read/write; data is retained when the application exits and when the system reboots</td>
<td>Data size is limited. Each channel has access to only 16kb of registry space.</td>
</tr>
</tbody>
</table>

1. ## [[Cachefs]]
3. ##  [[Pathnames]]

