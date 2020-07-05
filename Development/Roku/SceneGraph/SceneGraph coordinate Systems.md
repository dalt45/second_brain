# SceneGraph coordinate Systems

Each renderable node has a local coordinate system associated with it with an origin at (0,0) with x increasing left-to-right and y increasing top-to-bottom.

Each node can also have a 2D transformation specified that transform its local coordinate system into a transformed coordinate system.

> Similar to tranform CSS Property??, check if the recalculations are only done in the target node 

In the Roku SceneGraph implementation a [[node transformation matrix]] is specified by setting the values of four fields:

<table>
<thead>
<tr>
<th class="short-line">Field</th>
<th class="short-line">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="short-line">translation</td>
<td class="long-line">2D vector that describes an [x, y] offset of the local coordinate system origin</td>
</tr>
<tr>
<td class="short-line">scale</td>
<td class="long-line">2D vectors that describes an [x, y] scaling of the local coordinate system</td>
</tr>
<tr>
<td class="short-line">rotation</td>
<td class="long-line">Floating point value that describes a Z-axis rotation of the local coordinate system. The value is specified in radians with positive values representing a counter-clockwise rotation.</td>
</tr>
<tr>
<td class="short-line">scaleRotateCenter</td>
<td class="long-line">2D vector that describes a point in the local coordinate system that serves as the center of scaling and rotation</td>
</tr>
</tbody>
</table>

Each of these fields can be combined into an overall 2D transformation for the node by first applying these steps:

1. Translate by the inverse of the scale/rotate center
2. Multiplying by the scale amount
3. Apply the Z-axis rotation
4. Translate by the scale/rotate center
5. Translate by the translation amount.

In matrix math, the [[overall matrix]] is:

   `M = C(-1) S R C T`
Where:
- `M = Total Matrix`
- `C = 2D Traslation Matrix` describes the location of the scale/rotation center in the node local coordinate system
- `S = 2D Scaling Matrix` 
- `R = 2D rotation matrix`
- `T = 2D traslation matrix`

As the SceneGraph is traversed, 2D transformations are accumulated so that each child local coordinate system is transformed not only by its own 2D transformation matrix, but also the accumulated transformation matrix of all of its ancestors in the tree structure.

> Check complexity of applying traslation to a parent and child.

Resource: How is the  [[CSS transform]] PROPERTY calculated.

The transformation accumulation allows node classes to be developed without regard to their [[absolute pixel coordinates]]. Instead, each node can be have a layout relative to its local coordinate system, with its absolute on-screen position, size and orientation determined by the accumulated transformation matrix
