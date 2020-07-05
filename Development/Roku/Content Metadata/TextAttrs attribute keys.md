# [[TextAttrs attribute keys]]

<table>
<thead>
<tr>
<th class="short-line">Key</th>
<th class="short-line">Type</th>
<th class="short-line">Values</th>
<th class="short-line">Example</th>
</tr>
</thead>
<tbody>
<tr>
<td class="short-line">Color</td>
<td class="short-line">String</td>
<td class="long-line">roImageCanvas (applies to text and other colors): A color can be specified as an opaque color 24-bit RGB value (#RRGGBB) or as a color with alpha 32-bit ARGB value (#AARRGGBB). AA (alpha), RR (red), GG (green), and BB (blue) are 8-bit values specified as hexadecimal values 00..FF. When specified as a 32-bit color, the alpha channel bits in the color value range from 00=transparent to FF=opaque. The alpha channel enables blending the background with the images; Default: "#FFFFFF" (opaque white)</td>
<td class="short-line">"#FF0033FF"</td>
</tr>
<tr>
<td class="short-line">Font</td>
<td class="short-line">String</td>
<td class="long-line">roImageCanvas (applies to text): "Small","Medium","Large", or "Huge"; Default: "Medium". Also can use any fonts registered by the roFontRegistry Object and returned by its Get() method</td>
<td class="short-line">"Large"</td>
</tr>
<tr>
<td class="short-line">HAlign</td>
<td class="short-line">String</td>
<td class="long-line">roImageCanvas (applies to text): Controls the horizontal alignment of the text in the TargetRect. Options are: "Left", "HCenter" / "Center" /  "Middle", "Right", "Justify"; Default: "HCenter"</td>
<td class="short-line">"Right"</td>
</tr>
<tr>
<td class="short-line">VAlign</td>
<td class="short-line">String</td>
<td class="long-line">roImageCanvas (applies to text): Controls the vertical alignment of the text in the TargetRect. Options are: "Top", "VCenter" / "Center" / "Middle", "Bottom"; Default: "VCenter"</td>
<td class="short-line">"Bottom"</td>
</tr>
<tr>
<td class="short-line">TextDirection</td>
<td class="short-line">String</td>
<td class="long-line">roImageCanvas (applies to text): "LeftToRight" or "RightToLeft"; Default: "LeftToRight"</td>
<td class="short-line">"RightToLeft"</td>
</tr>
</tbody>
</table>