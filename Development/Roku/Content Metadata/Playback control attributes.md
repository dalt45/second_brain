# Playback control attributes

The playback control meta-data attributes are used to control the playback parameters for the content item.

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
<td class="short-line">MinBandwidth</td>
<td class="short-line">Integer</td>
<td class="long-line">roVideoPlayer or roVideoScreen: Will only select variant streams with a bandwidth higher than this minimum bandwidth. Units are kbps. By default Wowza servers set streams to 64 kbs, so you might want to set this parameter to something smaller than 64 when first testing Wowza streams. You will eventually want to specify the Wowza bitrates with a smil file (Please see the encoding guide)</td>
<td class="short-line">48</td>
</tr>
<tr>
<td class="short-line">MaxBandwidth</td>
<td class="short-line">Integer</td>
<td class="long-line">roVideoPlayer or roVideoScreen: Will only select variant streams with a bandwidth less than this maximum bandwidth. Units are kbps</td>
<td class="short-line">2500</td>
</tr>
<tr>
<td class="short-line">AudioPIDPref</td>
<td class="short-line">Integer</td>
<td class="long-line"><strong>This attribute is deprecated</strong><br><br>Users can select their preferred audio language on-device in the <strong>Settings &gt; Audio &gt; Audio Preferred Language</strong> screen.</td>
<td class="short-line">483</td>
</tr>
<tr>
<td class="short-line">FullHD</td>
<td class="short-line">Boolean</td>
<td class="long-line">roVideoPlayer or roVideoScreen: Specify that this stream was encoded at 1080p resolution</td>
<td class="short-line">true</td>
</tr>
<tr>
<td class="short-line">FrameRate</td>
<td class="short-line">Integer</td>
<td class="long-line">roVideoPlayer or roVideoScreen: Specify the 1080p stream was encoded at 24 or 30 fps</td>
<td class="short-line">24</td>
</tr>
</tbody>
</table>