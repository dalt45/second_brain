# SceneGraph certificate attributes

The SceneGraph certificate meta-data attributes are used to configure the use of HTTP certificates and cookies by the Audio and Video nodes.

<table>
<thead>
<tr>
<th class="short-line">Attribute</th>
<th class="short-line">Type</th>
<th class="short-line">Values</th>
</tr>
</thead>
<tbody>
<tr>
<td class="short-line">HttpCertificatesFile</td>
<td class="short-line">uri</td>
<td class="long-line">If set, the Scene Graph Audio or Video node loads this public certificate bundle, to authenticate the server. The protocol must be https for this to have any effect. When used with a Scene Graph Audio or Video node, the node or global HttpAgent is found, as explained elsewhere in this documentation. When playing this content, the agent is updated in the following manner: <ul>
<li>If this attribute is defined, the file URI is set into the HttpAgent instance. However, if this attribute is specified and the value is the empty string (""), then no changes will be made to the HttpAgent.</li>
<li>
<p>If this attribute is not defined, the behavior depends upon whether the Content Meta-Data (CMD) contains secure (https) URLs:</p>
<ul>
<li>If no secure URLs exist in the meta-data, then no certificates file path is set into the agent.</li>
<li>If a secure URL does exist, the platform's default certificates are set into the agent.</li>
</ul>
</li>
</ul></td>
</tr>
<tr>
<td class="short-line">HttpCookies</td>
<td class="short-line">array of strings</td>
<td class="long-line">If set, the Scene Graph Audio or Video node send the cookies to the server. Each cookie must have the following syntax: dom=domain;path=path;name=name;val=value; When used with a Scene Graph Audio or Video node, the node or global HttpAgent is found, as explained elsewhere in this documentation. When this Content Meta-Data is played and this attribute is set, all HTTP cookies in the agent are cleared and replaced with the cookies defined by this attribute</td>
</tr>
<tr>
<td class="short-line">HttpHeaders</td>
<td class="short-line">array of strings</td>
<td class="long-line">If set, the Scene Graph Audio or Video node sends these headers to the server. Each string must be of the format "name:value". When used with a Scene Graph Audio or Video node, the node or global HttpAgent is found, as explained elsewhere in this documentation. When this Content Meta-Data is played and this attribute is set, all HTTP headers in the agent are cleared and replaced with the headers defined by this attribute</td>
</tr>
<tr>
<td class="short-line">HttpSendClientCertificate</td>
<td class="short-line">Boolean</td>
<td class="long-line">If true, the Scene Graph Audio or Video node sends the client device certificate to the server, for client authentication. The protocol must be https for this to have any effect. When used with a Scene Graph Audio or Video node, the node or global HttpAgent is found, as explained elsewhere in this documentation. When this Content Meta-Data is played and this attribute exists, the value of this attribute (true or false) is set into the HttpAgent</td>
</tr>
</tbody>
</table>