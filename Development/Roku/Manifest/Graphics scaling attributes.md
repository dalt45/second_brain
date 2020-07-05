# Graphics scaling attributes

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
<td><code>ui_resolutions</code></td>
<td>comma separated values</td>
<td>A comma-separated list of up to three strings that identify the UI resolutions the application has been designed to support.</td>
<td><code>ui_resolutions=sd,hd,fhd</code></td>
</tr>
<tr class="even">
<td><code>uri_resolution_autosub</code></td>
<td>comma separated values</td>
<td>Provides a flexible way to specify graphical image URIs that are automatically modified to replace a specified string with a string that gets a resolution-specific graphical image.<br />
<br />
The attribute value is a comma-separated list of four strings that specify the string to be replaced along with the replacement strings for SD, HD and FHD resolutions. For example, suppose the manifest includes this line: <code>uri_resolution_autosub=$$RES$$,SD,720p,1080p</code> And the Roku player supports full high-definition resolution. Then if the application specifies a URI of: <a href="http://www.roku.com/testChannel/assets/$$RES$$/rokuTV.jpg">http://www.roku.com/testChannel/assets/$$RES$$/rokuTV.jpg</a>. At runtime that URI will be modified to: <a href="http://www.roku.com/testChannel/assets/1080p/rokuTV.jpg">http://www.roku.com/testChannel/assets/1080p/rokuTV.jpg</a> and the application will get the full-high definition version of the graphical image in the specified directory.</td>
<td><code>uri_resolution_autosub=$$RES$$,SD,720p,1080p</code></td>
</tr>
</tbody>
</table>

1.  The default setting for `ui_resolutions` is `ui_resolutions=sd,hd`
    
      - `sd` Applications designed for standard definition 720x480
      - `hd` Applications designed for high definition 1280x720
      - `fhd`Applications designed for full high definition 1920x1080