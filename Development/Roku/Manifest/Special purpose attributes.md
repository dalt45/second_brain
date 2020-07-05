# Special purpose attributes

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
<td><code>hidden</code></td>
<td>integer</td>
<td>The hidden property tells the Roku OS to not display the app on the home screen. Hidden apps can still be launched over the network via the <a href="/docs/developer-program/debugging/external-control-api.md">External Control API</a>.</td>
<td><code>hidden=1</code></td>
</tr>
<tr class="even">
<td><code>playonly_aware</code></td>
<td>integer</td>
<td>Attribute to specify the application responds to the Play Only remote control button event. If not set, the application will receive the Play event instead when the user selects the button.</td>
<td><code>playonly_aware=1</code></td>
</tr>
<tr class="odd">
<td><code>rsg_version</code></td>
<td>value</td>
<td>Sets the SceneGraph <a href="/docs/developer-program/core-concepts/handling-application-events.md">observer callback model</a>.<br />
<br />
If using Roku OS 9.0 or above, use <code>rsg_version=1.2</code>. This enables a new internal mechanism for processing component &lt;script&gt; tags that optimizes the resulting compiled script code resulting in a reduced initial startup time and lesser memory usage while preserving compatibility.<br />
<br />
If using a <a href="/docs/references/scenegraph/control-nodes/componentlibrary.md">Roku component library node</a>, the <code>rsg_version</code> flag needs to be declared in the component library's manifest as well.<br />
<br />
<a href="/docs/references/brightscript/language/runtime-functions.md#evalcode-as-string-as-dynamic">Eval()</a> is deprecated. Eval() cannot be used with <code>rsg_version=1.2</code>.<br />
<br />
The manifest entry defaults to 1.2 as of Roku OS 9.3 if it's not specified in the manifest.<br />
<br />
Note that support for the “rsg_version=1.0” manifest flag is deprecated as of Roku OS 8.</td>
<td><code>rsg_version=1.2</code></td>
</tr>
<tr class="even">
<td><code>automatic_audio_guide_disabled</code></td>
<td>integer</td>
<td>Set to 1 to disable Audio Guide within a channel.</td>
<td><code>automatic_audio_guide_disabled=1</code></td>
</tr>
<tr class="odd">
<td><code>bs_prof_enabled</code></td>
<td>boolean</td>
<td>Enable <a href="/docs/developer-program/dev-tools/brightscript-profiler.md">BrightScript profiling</a></td>
<td><code>bs_prof_enabled=true</code></td>
</tr>
<tr class="even">
<td><code>confirm_partner_button</code></td>
<td>integer</td>
<td>This new feature has been added that launches a confirmation dialogue before launching a channel when the user presses one of the four channel-specific buttons on the Roku remote. This minimizes the number of unintended channel launches after accidentally hitting a button while fast forwarding or rewinding content in a different channel. When this manifest flag is set to “1” (confirm_partner_button=1), the OS will display a confirmation HUD (Head Up Display) any time the user presses a partner channel button while in that app. By default, the OS will always display this confirmation HUD when a partner button is pressed during video playback, regardless of if the manifest flag has been set. <img src="https://image.roku.com/ZHZscHItMTc2/confirmpartnerbutton.jpg" alt="confirm partner button" /></td>
<td><code>confirm_partner_button=1</code></td>
</tr>
<tr class="odd">
<td><code>suppress_unconnected_hud</code></td>
<td>integer</td>
<td>Manifest entry for overriding network connectivity HUD. This attribute is used to override the system level display that indicates when media playback is interrupted due to network connection failures. <em>For more information on the connectivity HUD, please read the related <a href="https://support.roku.com/article/208755728-what-to-do-if-you-can">support article</a></em></td>
<td><code>suppress_unconnected_hud=[1|0]</code><br />
<br />
(1 suppresses, 0 enables).</td>
</tr>
<tr class="even">
<td><code>dial_title</code></td>
<td>string</td>
<td>The name of the title used by the Roku <a href="/docs/developer-program/debugging/external-control-api.md#dial-discovery-and-launch">DIAL</a> server to identify the channel.</td>
<td><code>dial_title=2Dvideo</code></td>
</tr>
<tr class="odd">
<td><code>game</code></td>
<td>integer</td>
<td><em>Available since Roku OS 9</em><br />
<br />
All game channels must add the game manifest entry to their manifest file. This flag prevents the channel from having audio/sound effects delays in the game.</td>
<td><code>game=1</code></td>
</tr>
</tbody>
</table>