# CDN Switching
Content Delivery Networks (CDNs) can be switched during playback to load balance traffic and failover to different servers in order to help optimize performance. The CdnConfig attribute can be used for managing load balancing and failovers.

<table>
<thead>
<tr>
<th class="short-line">Attribute</th>
<th class="short-line">Type</th>
<th class="short-line">Values</th>
<th class="short-line">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="short-line">CdnConfig</td>
<td class="short-line">roArray of roAssociativeArrays</td>
<td class="long-line"><div class="hscroll"><table>
<thead>
<tr>
<th class="short-line">Key</th>
<th class="short-line">Required/ Optional</th>
<th class="short-line">Type</th>
<th class="short-line">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="short-line"><strong>URLFilter</strong></td>
<td class="short-line">Required</td>
<td class="short-line">String</td>
<td class="long-line">A substring that identifies the (base)URL to which these CDN settings apply. <br><br>The Roku media player matches this string against all (base)URLs listed in the manifest and applies the setting to all (base)URLs that contain this substring.</td>
</tr>
<tr>
<td class="short-line"><strong>ContentFilter</strong></td>
<td class="short-line">Optional</td>
<td class="short-line">String</td>
<td class="long-line">For DASH streams, a substring that filters the period or asset ID to which these CDN settings apply.<br><br> The Roku player only applies these CDN setting to periods with a period ID or asset ID that contains this substring. <br><br>This match is used in addition to the URL filter.</td>
</tr>
<tr>
<td class="short-line"><strong>Priority</strong></td>
<td class="short-line">Required</td>
<td class="short-line">Integer</td>
<td class="long-line">For configuring failovers, sets the priority for this (base)URL from 1 to x (a priority of 0 or less is invalid). <br><br>A lower value indicates a higher priority. For example, a (base)URL with a priority of 1 is higher than another with a priority of 10. <br><br>If the highest priority server fails, traffic is routed to the server with the next highest priority. If all servers are configured with the same priority, and one fails, no failover will happen.</td>
</tr>
<tr>
<td class="short-line"><strong>Weight</strong></td>
<td class="short-line">Required</td>
<td class="short-line">Integer</td>
<td class="long-line">For configuring load balancing, sets the relative weight for all (base)URLs with the same priority. This must be a value of 1 or greater (a weight of 0 disables a CDN). <br><br>The weight of a given BaseURL is its weight value divided by the sum of all weight values. This means that to spread the load equally across multiple CDNs with the same priority, set the weight for each to the same value. To configure the weights for two servers to 80% and a third server to 20%, for example, set servers one and two to 8 and server three to 4.</td>
</tr>
<tr>
<td class="short-line"><strong>ServiceLocation</strong></td>
<td class="short-line">Optional</td>
<td class="short-line">String</td>
<td class="short-line">A blacklist of failed BaseURL locations.</td>
</tr>
</tbody>
</table></div></td>
<td class="long-line">To update the configuration of a CDN listed in this attribute, call the <strong>roVideoPlayer.UpdateContent()</strong> method.<br><br>The <strong>URLFilter</strong>, <strong>Priority</strong>, and <strong>Weight</strong> attributes must be specified to apply these configurations.</td>
</tr>
</tbody>
</table>