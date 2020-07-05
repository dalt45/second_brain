# Digital rights management (DRM) control attributes

Digital rights management (DRM) content meta-data control attributes are available in the Roku OS through the drmParams parameter of type roAssociativeArray. The table below enumerates all usable attributes of drmParams.

<table>
<thead>
<tr>
<th class="short-line">Attribute</th>
<th class="short-line">DRM System</th>
<th class="short-line">Type</th>
<th class="short-line">Value</th>
<th class="short-line">Example</th>
</tr>
</thead>
<tbody>
<tr>
<td class="short-line">appData</td>
<td class="short-line">Playready, Widevine, Verimatrix: Optional</td>
<td class="short-line">String</td>
<td class="long-line">Special meaning per DRM system. If supplied, expected to be a base64 encoded string.</td>
<td class="short-line">"SGF2ZSB0byBkZWFsIHdpdGggQmFzZTY0IGZ..."</td>
</tr>
<tr>
<td class="short-line">encodingKey</td>
<td class="short-line">Playready: Optional</td>
<td class="short-line">String</td>
<td class="long-line">This field is deprecated; use the <strong>licenseServerURL</strong> field.<br><br>Specifies the PlayReady license acquisition data, in format depending on the EncodingType attribute value specified:<br><ul>
<li>when encodingType="PlayReadyLicenseAcquisitionUrl", the EncodingKey attribute contains the PlayReady license acquisition URL</li>
</ul></td>
<td class="long-line">"<a href="http://serverName/">http://serverName/</a></td>
</tr>
<tr>
<td class="short-line">encodingType</td>
<td class="short-line">Playready: Optional</td>
<td class="short-line">String</td>
<td class="long-line">This field is deprecated; use the <strong>licenseServerURL</strong> field.<br><br>Specifies the encoding scheme for PlayReady DRM, by setting to one of the following values:<br><ul>
<li>"PlayReadyLicenseAcquisitionUrl"</li>
<li>"PlayReadyLicenseAcquisitionAndChallenge"  Note, this is the same value that used to be specified directly in Content Metadata structure</li>
</ul></td>
<td class="short-line">"PlayReadyLicenseAcquisitionAndChallenge"</td>
</tr>
<tr>
<td class="short-line">KeySystem</td>
<td class="short-line">Required for all</td>
<td class="short-line">String</td>
<td class="long-line">"playready", "widevine", or "verimatrix". This value is case-insensitive. The default is an empty string.</td>
<td class="short-line">"widevine"</td>
</tr>
<tr>
<td class="short-line">licenseRenewURL</td>
<td class="short-line">Widevine: Optional</td>
<td class="short-line">String</td>
<td class="long-line">A URL location for sending license renewal requests. If not specified, the Roku OS would send renewal requests to the URL specified in the licenseServerURL.</td>
<td class="long-line">" <a href="https://host.com/license/wideivne/renew?licenseid=090495867002">https://host.com/license/wideivne/renew?licenseid=090495867002</a> "</td>
</tr>
<tr>
<td class="short-line">licenseServerURL</td>
<td class="short-line">Playready: Required Widevine: Required</td>
<td class="short-line">String</td>
<td class="long-line">A URL location of a license server. This URL may include CGI parameters.<br><br>If this field contains the PlayReady license acquisition URL plus additional custom license acquisition request data in format "URL%%%",  the “PlayReadyLicenseAcquisitionAndChallenge" type is used.</td>
<td class="long-line">"<a href="https://host.com/license/playready?contentid=090495867002">https://host.com/license/playready?contentid=090495867002</a> "</td>
</tr>
<tr>
<td class="short-line">serializationURL</td>
<td class="short-line">Verimatrix: Required Playready, Widevine: Optional</td>
<td class="short-line">String</td>
<td class="short-line">A server address used for device provisioning</td>
<td class="long-line">"<a href="https://host.com/provision/device?esn=090495867002">https://host.com/provision/device?esn=090495867002</a> "</td>
</tr>
<tr>
<td class="short-line">serviceCert</td>
<td class="short-line">Widevine: Optional Others: N/R (leave unset)</td>
<td class="short-line">String</td>
<td class="long-line">The actual certificate string for Widevine purposes, which must be obtained out-of-band (OOB) by the channel. Leave this unset unless Widevine is used for DRM.</td>
<td class="long-line">Certificate strings are too long to display here. Examples can be fetched from such sources as the Widevine test license server at "<a href="https://proxy.uat.widevine.com/proxy">https://proxy.uat.widevine.com/proxy</a>. "</td>
</tr>
</tbody>
</table>