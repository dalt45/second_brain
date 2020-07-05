SceneGraph, nodes can either be [[renderable nodes]] or [[non-renderable nodes]].

## Renderable Nodes
-  Renderable nodes are arranged in the tree structure that is traversed during rendering to draw the scene
-  3 basic types of nodes that actually draw something
	- [[Rectangle node]] renders a rectangle on the display screen
	- [[Label node]] renders a formatted string of text to the display screen
	- A [[Poster node]] renders a graphical image to the display screen   

## Non-Renderable Nodes
- Non-renderable nodes are ignored during the render traversal, and are used to describe other information used by the scene, such as timers, animations, and data to be displayed.

## [[SceneGraph coordinate Systems]]

## Inherited Properties
In addition to inheriting a [[trasnformation matrix]]from its parent, each node in the SceneGraph also inherits visibility and opacity information. (Opacity is the opposite of transparency: 75% opacity is the same as 25% transparency.) The visible field stores a Boolean value that provides a way to switch rendering of the node and all of its descendants on and off. The opacity field specifies an opacity value that is multiplied with the accumulated opacity of its parents to allow branches of the SceneGraph to fade in and out.

## [[Node field observers]]
All node and component fields can have observers attached to them.