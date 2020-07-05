## Overview
The term [[SceneGraph]] refers to a design algorithm and associated programming constructs that are widely used in computer graphics systems, such as video games.

A SceneGraph uses a tree structure of image element nodes to define an interactive scene that is traversed to render an image, with the position of each node in the tree determining the z-axis rendering of the node image element; [[SceneGraph nodes]] lower in the tree structure are rendered over nodes higher in the tree. 

Each node in the tree structure is an object whose state is stored as attributes in a set of [[fields]].

### XML definition of a SceneGraph tree
- Roku SceneGraph uses [[XML]] files to define the attributes of all [[SceneGraph nodes]].
- The attribute fields are strongly typed and can include arbitrary data, including floating point numbers, integers, strings, Boolean values, 2D vectors, and pointers to other nodes.
-  Fields can have animations attached to them that allow the property represented by the field to be smoothly interpolated through a set of key values.

## Key events/rendering optimization

The SceneGraph algorithm is useful in other ways including:
- #### Supporting key event propagation
A node in the graph is given remote control key focus and receives key events. If that node does not handle the particular key event, the event is passed up the SceneGraph to its parent node, until it reaches a node that handles the event.

> Bubbling and Capturing alike 

- #### Rendering Optimization
Roku SceneGraph uses a render culling algorithm that allows entire branches of the SceneGraph to not be traversed for rendering if the bounding rectangle of the root of that branch is outside the viewable area of the TV display screen, allowing much quicker and more efficient scene rendering.


