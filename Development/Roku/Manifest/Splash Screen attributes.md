# Splash Screen attributes

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
<td><code>splash_color</code></td>
<td>hex value</td>
<td>background color to use if the splash screen image is not full screen</td>
<td><code>splash_color=#121212</code></td>
<td></td>
</tr>
<tr class="even">
<td><code>splash_min_time</code></td>
<td>integer</td>
<td>minimum amount of time (in milliseconds) to display the splash screen<br />
<br />
If no value is specified, then 1600 (1.6 seconds) is used. If 0 is specified, then there is no default time, so the splash screen disappears as soon as the application displays its first screen. (This may result in the appearance of flashing, if your application shows its first screen quickly).</td>
<td><code>splash_min_time=1500</code></td>
<td></td>
</tr>
<tr class="odd">
<td><code>splash_screen_fhd</code></td>
<td>string</td>
<td>local URI for the FHD splash screen<br />
<br />
The FHD splash screen image is scaled down for HD display mode but this attribute can be used to specify a resolution-specific splash screen image.</td>
<td><code>splash_screen_fhd=pkg:/images/splash-screen_FHD.png</code></td>
<td>1920x1080</td>
</tr>
<tr class="even">
<td><code>splash_rsg_optimization</code></td>
<td>integer</td>
<td>Roku recommends that you do not use this attribute at this time as it may deplete your channel's available memory resources. Set this attribute to remove the black screen flash in SceneGraph channels. This is only applicable for SceneGraph channels and only if the first screen is a SceneGraph component.</td>
<td><code>splash_rsg_optimization=1</code></td>
<td></td>
</tr>
</tbody>
</table>