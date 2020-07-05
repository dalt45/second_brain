# Track ID attributes

<table>
<thead>
<tr>
<th class="short-line">Attribute</th>
<th class="short-line">Type</th>
<th class="short-line">Values</th>
<th class="short-line">Example</th>
</tr>
</thead>
<tbody>
<tr>
<td class="short-line">TrackIDAudio</td>
<td class="short-line">String</td>
<td class="long-line">roVideoPlayer or roVideoScreen: Used in SmoothStreaming (StreamFormat = "ISM") to specify. Set the TrackIDAudio field to the desired track's StreamIndex.Name attribute from the manifest file</td>
<td class="short-line">"Spanish"</td>
</tr>
<tr>
<td class="short-line">TrackIDVideo</td>
<td class="short-line">String</td>
<td class="long-line">roVideoPlayer or roVideoScreen: Used in SmoothStreaming (StreamFormat = "ISM") to specify. Set the TrackIDVideo field to the desired track's StreamIndex.Name attribute from the manifest file</td>
<td class="short-line">"h264video"</td>
</tr>
<tr>
<td class="short-line">TrackIDSubtitle</td>
<td class="short-line">String</td>
<td class="long-line">roVideoPlayer: Used to specify a closed caption track in a video stream that supports 608/708 captions</td>
<td class="short-line">"eia608/1"</td>
</tr>
<tr>
<td class="short-line">AudioFormat</td>
<td class="short-line">String</td>
<td class="long-line">roSpringboardScreen: If set to "dolby-digital", will display a "5.1 ))" icon in the lower left of a movie style springboard screen</td>
<td class="short-line">"dolby-digital"</td>
</tr>
<tr>
<td class="short-line">AudioLanguageSelected</td>
<td class="short-line">String</td>
<td class="long-line"><strong>This attribute was deprecated as of the Roku 9.2 OS release.</strong> <br><br>Users can select their preferred audio language on-device in the <strong>Settings &gt; Audio &gt; Audio Preferred Language</strong> screen.</td>
<td class="short-line">"eng"</td>
</tr>
</tbody>
</table>