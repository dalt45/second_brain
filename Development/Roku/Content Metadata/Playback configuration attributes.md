# Playback configuration attributes

Playback configuration meta-data attributes are used to configure the playback of the content item.

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
<td class="short-line">Live</td>
<td class="short-line">Boolean</td>
<td class="long-line">Optional flag indicating video is live. Replaces time remaining in progress bar to display "Live". Default is false</td>
<td class="short-line">True</td>
</tr>
<tr>
<td class="short-line">Url</td>
<td class="short-line">String</td>
<td class="long-line">Image URL for roSlideShow or roImageCanvas, stream URL for Scene Graph Video node</td>
<td class="long-line"><a href="http://www.myco.com/img/vacation.jpg">http://www.myco.com/img/vacation.jpg</a></td>
</tr>
<tr>
<td class="short-line">SDBifUrl</td>
<td class="short-line">String</td>
<td class="short-line">BIF URL for SD trick mode</td>
<td class="long-line"><a href="http://www.myco.com/bif/sd1932.bif">http://www.myco.com/bif/sd1932.bif</a></td>
</tr>
<tr>
<td class="short-line">HDBifUrl</td>
<td class="short-line">String</td>
<td class="short-line">BIF URL for HD trick mode</td>
<td class="long-line"><a href="http://www.myco.com/bif/hd1932.bif">http://www.myco.com/bif/hd1932.bif</a></td>
</tr>
<tr>
<td class="short-line">FHDBifUrl</td>
<td class="short-line">String</td>
<td class="short-line">BIF URL for FHD trick mode</td>
<td class="long-line"><a href="http://www.myco.com/bif/fhd1932.bif">http://www.myco.com/bif/fhd1932.bif</a></td>
</tr>
<tr>
<td class="short-line">Stream</td>
<td class="short-line">roAssociativeArray</td>
<td class="long-line">Supported by roVideoPlayer and roVideoScreen, but not the Roku Scene Graph Video node.<br>For the Video node, use the top level url, streamformat, etc. attributes. <br><br>The exception is cases where you don't have adaptive streams (typically MP4) and need to specify different bitrate variants separately. For this use case use the Streams attribute. roAssociativeArray that has parameters representing the stream settings that were set as individual roArrays in previous firmware revisions. <br><br>The old method is still supported and descriptions of the parameters can be found under those content-meta data entries. <br><br>For url please see StreamUrls, for quality it is now a Boolean that is true for HD quality. <br><div class="hscroll"><table>
<thead>
<tr>
<th class="short-line">Key</th>
<th class="short-line">Type</th>
</tr>
</thead>
<tbody>
<tr>
<td class="short-line">url</td>
<td class="short-line">String</td>
</tr>
<tr>
<td class="short-line">stickyredirects</td>
<td class="short-line">Boolean</td>
</tr>
<tr>
<td class="short-line">quality</td>
<td class="short-line">Boolean</td>
</tr>
<tr>
<td class="short-line">contentid</td>
<td class="short-line">String</td>
</tr>
<tr>
<td class="short-line">bitrate</td>
<td class="short-line">Integer</td>
</tr>
</tbody>
</table></div></td>
<td class="long-line">{ url : "<a href="http://me.com/big.m3u8%22">http://me.com/big.m3u8"</a>, quality : true, contentid : "big-hls" }</td>
</tr>
<tr>
<td class="short-line">Streams</td>
<td class="short-line">roArray of roAssociativeArrays</td>
<td class="long-line">Used by roVideoPlayer and roVideoScreen to specify the content metadata for a set of fixed bitrate streams.<br><br>Each array item specifies the URL, bitrate, etc. for one stream variant. <br><br>Setting stream content metadata using the Streams value is recommended for non-adaptive video (such as MP4 progressive download) only.<br><br>For adaptive streaming, use the Stream metadata value.<br><div class="hscroll"><table>
<thead>
<tr>
<th class="short-line">Key</th>
<th class="short-line">Type</th>
</tr>
</thead>
<tbody>
<tr>
<td class="short-line">url</td>
<td class="short-line">String</td>
</tr>
<tr>
<td class="short-line">stickyredirects</td>
<td class="short-line">Boolean</td>
</tr>
<tr>
<td class="short-line">quality</td>
<td class="short-line">Boolean</td>
</tr>
<tr>
<td class="short-line">contentid</td>
<td class="short-line">String</td>
</tr>
<tr>
<td class="short-line">bitrate</td>
<td class="short-line">Integer</td>
</tr>
</tbody>
</table></div></td>
<td class="long-line">[ { url : "http://me.com/x-384.mp4",  bitrate : 384, quality : false, contentid : "x-384" },  { url : "http://me.com/x2500.mp4",  bitrate : 2500, quality : true, contentid : "x-1500" } ]</td>
</tr>
<tr>
<td class="short-line">StreamBitrates</td>
<td class="short-line">roArray</td>
<td class="long-line">Array of bitrates in kbps for content streams used. <br><br>Setting stream bitrates using this value is recommended for non-adaptive video (such as MP4 progressive download) only.<br><br><strong>Must be used in conjunction with StreamUrls and StreamQualities</strong></td>
<td class="short-line">[ 384, 500, 1000, 1500 ]</td>
</tr>
<tr>
<td class="short-line">StreamUrls</td>
<td class="short-line">roArray</td>
<td class="long-line">Array of URL's for content streams. <br><br>Setting stream urls using this value is recommended for non-adaptive video (such as MP4 progressive download) only.<br><br> <strong>Must be used in conjunction with StreamBitrates and StreamQualities</strong></td>
<td class="long-line">[ "http://www.myco.com/vid/1932-1.mp4", "http://www.myco.com/vid/1932-2.mp4", "http://www.myco.com/vid/1932-3.mp4", "http://www.myco.com/vid/1932-4.mp4" ]</td>
</tr>
<tr>
<td class="short-line">StreamQualities</td>
<td class="short-line">roArray</td>
<td class="long-line">Array of Strings quality indicators identifying a stream as "SD" or "HD". <br><br> <strong>Must be used in conjunction with StreamBitrates and StreamUrls</strong></td>
<td class="short-line">[ "SD", "SD", "SD", "HD" ]</td>
</tr>
<tr>
<td class="short-line">StreamContentIDs</td>
<td class="short-line">roArray</td>
<td class="long-line">Array of String values logged in Roku logs to identify stream and bitrate played</td>
<td class="long-line">[ "myco-19321-384.mp4", "myco-19321-500.mp4", "myco-19321-1000.mp4", "myco-19321-1500.mp4" ]</td>
</tr>
<tr>
<td class="short-line">StreamStickyHttpRedirects</td>
<td class="short-line">roArray</td>
<td class="long-line">Array of Boolean values indicating if the HTTP endpoint should be sticky and not subject to change on subsequent requests. Default is false</td>
<td class="short-line">[ false, false, false, false ]</td>
</tr>
<tr>
<td class="short-line">StreamStartTimeOffset</td>
<td class="short-line">Integer</td>
<td class="long-line">Optional. Default is 0. The offset into the stream which is considered the beginning of playback. Time in seconds.</td>
<td class="short-line">3600 (one hour)</td>
</tr>
<tr>
<td class="short-line">StreamFormat</td>
<td class="short-line">String</td>
<td class="long-line">Type of content <ul>
<li>
<p>Type of content:</p>
<ul>
<li>Default: H.264/AAC in .mp4 Container</li>
</ul>
</li>
<li>
<p>Valid values:</p>
<ul>
<li>"mp4" (mp4 will also accept .mov and .m4v files)</li>
<li>"wma"</li>
<li>"mp3"  </li>
<li>"hls"
-"ism" (smooth streaming)</li>
<li>"dash" (MPEG-DASH)</li>
<li>"mkv", "mka", "mks"</li>
</ul>
</li>
<li>
<p>Deprecated:</p>
<ul>
<li>"wmv"</li>
</ul>
</li>
</ul></td>
<td class="short-line"></td>
</tr>
<tr>
<td class="short-line">Length</td>
<td class="short-line">Integer</td>
<td class="long-line">Movie Length in Seconds; Length zero displays at 0m, Length not set will not display</td>
<td class="short-line">3600 (one hour)</td>
</tr>
<tr>
<td class="short-line">BookmarkPosition</td>
<td class="short-line">Integer</td>
<td class="long-line">BookmarkPosition sets the default start position, in seconds, for this content.<br><br>The player will start playback at this position in the content unless an explicit seek position was set. <br><br>An explicit seek position can be set by calling seek on the player or after a user has selected a starting point via the trickplay UI. <br><br>Users are allowed to seek to positions prior to BookmarkPostion in the content. This value takes precedence over the PlayStart value.<br><br><strong>Starting from Roku OS 8.1, this attribute is made obsolete. The existing PlayStart attribute does the same thing, and there is no need to have two attributes to set the play start time. the Roku OS will continue to support BookmarkPosition to maintain the backward compatibility, but channels should use PlayStart</strong></td>
<td class="short-line">1950 (32 minutes, 30 seconds)</td>
</tr>
<tr>
<td class="short-line">PlayStart</td>
<td class="short-line">Integer</td>
<td class="long-line">PlayStart defines the start position of the content, in seconds.<br><br>The player is not allowed to move to a position prior to this point. Any seek operation prior to this point will be clipped to PlayStart.<br><br>Channels can use PlayStart and PlayDuration to split one content piece into multiple clips and insert these clips with other content (typically advertisements) into one content list.<br><br>Starting from Roku OS 8.0, content metadata supports negative PlayStart values. This feature allows the media players to start playbacks distanced from the edge of the live stream</td>
<td class="short-line">0</td>
</tr>
<tr>
<td class="short-line">PlayDuration</td>
<td class="short-line">Integer</td>
<td class="long-line">Optional Playback Max Duration in Seconds. <strong>PlayDuration has been deprecated is is no longer used by the media player starting from Roku OS 8.1</strong></td>
<td class="short-line">120 (two minute preview)</td>
</tr>
<tr>
<td class="short-line">ClosedCaptions</td>
<td class="short-line">Boolean</td>
<td class="short-line">Boolean indicating if CC icon should be displayed</td>
<td class="short-line">True</td>
</tr>
<tr>
<td class="short-line">HDBranded</td>
<td class="short-line">Boolean</td>
<td class="long-line">Boolean indicating if HD branding should be displayed</td>
<td class="short-line">True</td>
</tr>
<tr>
<td class="short-line">IsHD</td>
<td class="short-line">Boolean</td>
<td class="short-line">Boolean indicating if content is HD</td>
<td class="short-line">True</td>
</tr>
<tr>
<td class="short-line">SubtitleColor</td>
<td class="short-line">String</td>
<td class="long-line">Theme metadata attribute that specifies the color to use when rendering subtitle text</td>
<td class="short-line">"#FF0000"</td>
</tr>
<tr>
<td class="short-line">SubtitleConfig</td>
<td class="short-line">roAssociativeArray: {TrackName : String}</td>
<td class="long-line">Specifies the caption settings for content playback.<br><br>TrackName sets the name of the caption track to render. This string is a concatenation of the track source and track id, separated by a "/".<br><br>Valid track sources are: "ism", "mkv", "eia608" and "dvb".<br><br>The track id must match the track identifier in the smooth or mkvmanifest. For example, if an mkvfile has a caption track called “english1” the TrackName to select this track is “mkv/english1”.<br><br>When the track source is "dvb", the track id is the three-letter language code, with "_sdh" appended for subtitles for the deaf and hard of hearing. For example, "dvb/eng_sdh" are English subtitles for the deaf and hard of hearing and "dvb/nor" are normal Norwegian subtitles.<br><br>For sideloaded caption tracks, the TrackName is the url from where the caption track can be downloaded.Sideloaded caption formats can include srt,ttml, anddfxp. Specifying eia608/1 will trigger the Roku OS to search for embedded 608/708 captions in the stream. In the 8.0 Roku OS, automatic track selection based on a preferred caption language setting is introduced. Omit setting a URL here to avoid interfering with the automatic track selection. It is sufficient to add the URLs to SubtitleTracks</td>
<td class="short-line">{ TrackName :  "mkv/english1" }</td>
</tr>
<tr>
<td class="short-line">SubtitleTracks</td>
<td class="long-line">roArray of roAssociativeArray: [{Language : String, Description : String, TrackName : String},...]</td>
<td class="long-line">SubtitleTracks sets the list of available caption tracks available to the stream. This list is added to the track list in the closed caption configuration dialog that is displayed during video playback when the user presses the Roku remote control * button. The captions from the selected track are then displayed on the screen. Language specifies the ISO 639.2B 3 character language code. This string is used to match the proper caption track with the audio language. Description specifies the text that will be shown for the corresponding track in the closed caption configuration dialog. For sideloaded caption tracks the TrackName is the URL from where the caption track can be downloaded. Sideloaded caption formats can include srt, ttml, and dfxp. The SubtitleTracks metadata is generally only used for side loaded captions. the Roku OS detects in-stream captions and thus specifying SubtitleTracks in this case is not necessary</td>
<td class="short-line"></td>
</tr>
<tr>
<td class="short-line">SubtitleUrl</td>
<td class="short-line">String</td>
<td class="long-line">Specifies the path to an SRT or TTML formatted file used to render subtitles or closed captions, respectively. This is supported on roVideoScreen only. See <a href="/docs/developer-program/media-playback/closed-caption.md">Closed Caption Support</a> for additional details</td>
<td class="long-line">"http:// www.myco.com/vid/1932.srt"; "<a href="http://www.myco.com/vid/1932.xml">http://www.myco.com/vid/1932.xml</a>"</td>
</tr>
<tr>
<td class="short-line">VideoDisableUI</td>
<td class="short-line">Boolean</td>
<td class="long-line">If set to true, hides the Scene Graph Video node trick play UI; If set to false (the default) shows the Scene Graph Video node trick play UI</td>
<td class="long-line">video = createObject("roSGNode", "Video"); video.content.VideoDisableUI = true</td>
</tr>
<tr>
<td class="short-line">EncodingType</td>
<td class="short-line">String</td>
<td class="long-line">Specifies the encoding scheme for PlayReady DRM, by setting to one of the following values: <ul>
<li>"PlayReadyLicenseAcquisitionUrl"</li>
<li>"PlayReadyLicenseAcquisitionAndChallenge"  Note, this is the same value that used to be specified directly in Content Metadata structure</li>
</ul></td>
<td class="short-line"></td>
</tr>
<tr>
<td class="short-line">EncodingKey</td>
<td class="short-line">String</td>
<td class="long-line">Specifies the PlayReady license acquisition URL, and additional custom request data, determined by the EncodingType attribute value specified: <ul>
<li>when encodingType="PlayReadyLicenseAcquisitionUrl", the EncodingKey attribute contains the PlayReady license acquisition URL</li>
</ul></td>
<td class="short-line"></td>
</tr>
<tr>
<td class="short-line">SwitchingStrategy</td>
<td class="short-line">String</td>
<td class="long-line">roVideoPlayer or roVideoScreen.<br><br>Specify different stream switching algorithms to be used in HLS adaptive streaming. <br>Only has an effect on HLS streams. "full-adaptation" uses measured bandwidth and buffer fullness to determine when to switch. This strategy requires that segments align across variants as the HLS spec requires. This is the new default</td>
<td class="short-line">"full-adaptation"</td>
</tr>
<tr>
<td class="short-line">Watched</td>
<td class="short-line">Boolean</td>
<td class="short-line">Flag indicating if content has been watched</td>
<td class="short-line">True</td>
</tr>
<tr>
<td class="short-line">ForwardQueryStringParams</td>
<td class="short-line">Boolean</td>
<td class="long-line">Controls whether query string parameters from initial HLS stream manifest requests are forward to subsequent segment download requests. The default value is set to true for backwards compatibility.</td>
<td class="short-line">True</td>
</tr>
<tr>
<td class="short-line">IgnoreStreamErrors</td>
<td class="short-line">Boolean</td>
<td class="long-line">When set to true the media player will not stop playback when it runs into a streaming related error for this content. Instead, it will skip to the next item in the content list.<br><br>If this was the last item in the content list the media player will send a regular completion event (like isFullResult). Channels are still notified of any errors via an isRequestFailed notification but a new attribute in the event’s GetInfo object tells the channel the error was ignored.<br><br>See the changes related to isRequestFailed for more information. The default value is false.</td>
<td class="long-line"><pre><code class="hljs language-json">video_details = {
    streamFormat: <span class="hljs-string">"mp4"</span>
    ignoreStreamErrors: <span class="hljs-literal">true</span>
    streams: [{bitrate: <span class="hljs-number">537</span>, height: <span class="hljs-number">360</span>, width: <span class="hljs-number">640</span>, url: “https:<span class="hljs-comment">//..."}]</span>
}</code></pre></td>
</tr>
<tr>
<td class="short-line">AdaptiveMinStartBitrate</td>
<td class="short-line">Integer</td>
<td class="long-line">Minimum startup bitrate specified in kbps. Streaming will start with a variant equal to or greater than this value. If this value is not set or if it's set to zero, any minimum start bitrate will be ignored.</td>
<td class="short-line">5000</td>
</tr>
<tr>
<td class="short-line">AdaptiveMaxStartBitrate</td>
<td class="short-line">Integer</td>
<td class="long-line">Maximum startup bitrate specified in kbps. Streaming will start with a variant less than or equal to this value. If this value is not set, it will default to 2500 kbps.</td>
<td class="short-line">2000</td>
</tr>
<tr>
<td class="short-line">filterCodecProfiles</td>
<td class="short-line">Boolean</td>
<td class="long-line">Filters out any video profile/codec level combinations that the specified hardware cannot play. The default value is false, in which case no filtering occurs. <strong>Note that this currently only works for DASH streams.</strong>  (Available since Roku OS 8.0)</td>
<td class="short-line">True</td>
</tr>
<tr>
<td class="short-line">LiveBoundsPauseBehavior</td>
<td class="short-line">String</td>
<td class="long-line">Allows a channel to customize Media Player behavior on live streams when playing in the earliest part of a DVR buffer.<br><br>The stream remains paused even though it is playing in the earliest part of the buffer of a live stream when the value of the attribute is set to "pause." This enables the Roku OS to distinguish between live streams and live streams that eventually transition to video on demand.<br><br>The possible values of this attribute are "resume", "stop", "pause", with resume being the default value.<br><br><strong>Currently, this attribute will work only with Smooth and Dash streams.</strong>  (Available since Roku OS 8.1)</td>
<td class="short-line">Resume</td>
</tr>
<tr>
<td class="short-line">ClipStart</td>
<td class="short-line">Float</td>
<td class="long-line">ClipStart sets the clip start position of the playback. The unit of ClipStart is seconds (Available since Roku OS 8.1).</td>
<td class="short-line">00.0</td>
</tr>
<tr>
<td class="short-line">ClipEnd</td>
<td class="short-line">Float</td>
<td class="long-line">ClipEnd sets the clip end position. The unit of ClipEnd is seconds (Available since Roku OS 8.1).</td>
<td class="short-line">00.0</td>
</tr>
<tr>
<td class="short-line">preferredaudiocodec</td>
<td class="short-line">String</td>
<td class="long-line">Specifies the audio codec that should be used during playback. The Media Player will select and report to the channel only those audio renditions that are encoded with the specified codec. Renditions that are encoded with a different codec are ignored. Possible values of this attribute are "aac", "ac3" and "eac3". (Available since Roku OS 9.0)</td>
<td class="short-line">"aac"</td>
</tr>
</tbody>
</table>