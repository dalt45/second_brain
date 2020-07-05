# [[roImageCanvas attributes]]

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
<td class="short-line">SourceRect</td>
<td class="long-line">Associative Array: {x : Integer, y : Integer, w : Integer, h : Integer}</td>
<td class="long-line">roImageCanvas: The rectangle from the image that should be drawn. The default is the entire image at the origin. <strong>Note the values must be of type Integer.  Other numeric types such as Float will be ignored and treated as 0.</strong> BrightScript returns a Float by default when doing division. You can convert calculated values to integer values using the Int() or Fix() functions, for example, if needed</td>
<td class="short-line">{x : 100, y : 100, w : 200, h : 200}</td>
</tr>
<tr>
<td class="short-line">TargetRect</td>
<td class="long-line">Associative Array: {x : Integer, y : Integer, w : Integer, h : Integer}</td>
<td class="long-line">roImageCanvas: The rectangle where the text/or image should be drawn. The default is the entire image at the origin. Can also be used with roFontMetrics to provide a target rect for the desired font size. <strong>Note the values must be of type Integer. Other numeric types such as Float will be ignored and treated as 0.</strong> BrightScript returns a Float by default when doing division.You can convert calculated values to integer values using the Int() or Fix() functions, for example, if needed</td>
<td class="short-line">{x : 400, y : 200, w : 200, h : 200}</td>
</tr>
<tr>
<td class="short-line">TargetTranslation</td>
<td class="short-line">Associative Array: {x : Integer, y : Integer}</td>
<td class="long-line">roImageCanvas: The amount to translate the coordinate system prior to drawing the image and/or text. Translation is done before rotation. Default: {0, 0}; <strong>Note the values must be of type Integer. Other numeric types such as Float will be ignored and treated as 0.</strong> BrightScript returns a Float by default when doing division. You can convert calculated values to integer values using the Int() or Fix() functions, for example, if needed</td>
<td class="short-line">{x : 100, y : 100}</td>
</tr>
<tr>
<td class="short-line">TargetRotation</td>
<td class="short-line">Float</td>
<td class="long-line">roImageCanvas: The angle (in degrees) to rotate the coordinate system prior to drawing the image and/or text. Default: 0</td>
<td class="short-line">90.0</td>
</tr>
<tr>
<td class="short-line">CompositionMode</td>
<td class="short-line">String</td>
<td class="long-line">roImageCanvas: Either "Source" (where source pixels completely replace destination pixels) or "Source_Over" (where source pixels are alpha blended with destination pixels)</td>
<td class="short-line">"Source_Over"</td>
</tr>
<tr>
<td class="short-line">Text</td>
<td class="short-line">String</td>
<td class="long-line">roImageCanvas: The text is drawn into the TargetRect</td>
<td class="short-line">"Hello ImageCanvas"</td>
</tr>
<tr>
<td class="short-line">TextAttrs</td>
<td class="short-line">Associative Array</td>
<td class="long-line">See <a href="/docs/developer-program/getting-started/architecture/content-metadata.md#textattrs-attribute-keys">TextAttrs Attribute Keys</a> for descriptions of the array keys</td>
<td class="long-line">{ Color : "#FFCCCCCC", Font : "Medium", HAlign : "HCenter", VAlign : "VCenter", Direction : "LeftToRight" }</td>
</tr>
</tbody>
</table>
