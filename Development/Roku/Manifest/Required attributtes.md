# [[Required attributtes]]
These are the minimum attributes required for every Roku channel:

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribute</th>
<th>Type</th>
<th>Description</th>
<th>Sample manifest entry</th>
<th>Specification</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><code>title</code></td>
<td>string</td>
<td>name of the channel</td>
<td><code>title=Roku Media Player</code></td>
<td></td>
</tr>
<tr class="even">
<td><code>major_version</code></td>
<td>integer</td>
<td>major portion of the channel version</td>
<td><code>major_version=1</code></td>
<td></td>
</tr>
<tr class="odd">
<td><code>minor_version</code></td>
<td>integer</td>
<td>minor portion of the channel version</td>
<td><code>minor_version=2</code></td>
<td></td>
</tr>
<tr class="even">
<td><code>build_version</code></td>
<td>integer</td>
<td>build number</td>
<td><code>build_version=00150</code></td>
<td></td>
</tr>
<tr class="odd">
<td><code>mm_icon_focus_hd</code></td>
<td>string</td>
<td>local URI for the HD channel icon.<br />
<br />
<strong>NOTE:</strong> The channel will not appear on devices or be accessible after publication without this attribute pointing to a valid image. The image's file name and file type must also match.</td>
<td><code>mm_icon_focus_hd=pkg:/images/channel-icon_HD.png</code></td>
<td>290x218</td>
</tr>
<tr class="even">
<td><code>mm_icon_focus_sd</code></td>
<td>string</td>
<td>local URI for the SD channel icon.<br />
<br />
<strong>NOTE:</strong> The channel will not appear on devices or be accessible after publication without this attribute pointing to a valid image. The image's file name and file type must also match.</td>
<td><code>mm_icon_focus_sd=pkg:/images/channel-icon_SD.png</code></td>
<td>246x140</td>
</tr>
<tr class="odd">
<td><code>splash_screen_hd</code></td>
<td>string</td>
<td>local URI for the HD splash screen displayed when the channel is launched</td>
<td><code>splash_screen_hd=pkg:/images/splash-screen_HD.png</code></td>
<td>1280x720</td>
</tr>
<tr class="even">
<td><code>splash_screen_sd</code></td>
<td>string</td>
<td>local URI for the SD splash screen displayed when the channel is launched</td>
<td><code>splash_screen_hd=pkg:/images/splash-screen_SD.png</code></td>
<td>720x480</td>
</tr>
</tbody>
</table>