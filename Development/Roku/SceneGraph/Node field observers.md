# Node field observers

The observers continuously monitor the state of the specified field, and if the field changes, a specified callback function is triggered to perform an action in response to the field state change.

In most cases, the observers are only notified if the field value changes. There is also loop breaking logic to make sure that you cannot get into an infinite loop of observer callbacks.

## Handling node field value changes
There are two [[ifSGNodeField]] methods that allow you to create (and remove) observers that continuously monitor any field value of any [[roSGNode]] object, including the interface fields you have created for custom SceneGraph components:

- `observerField()``
- `unobserveField()`

> Similar to `addEventListener()` or `MutationObserver()` [Mutation Observer -Developer Mozilla ](https://developer.mozilla.org/en-US/docs/Web/API/MutationObserver) 

`observeField()` is an overloaded method with two versions, useful for different purposes. 

**The first** allows you to trigger a specified callback function in response to **any change** in the value of the observed node field.

**The second** version of observeField() lets you specify a message port to notify when the observed field changes:

 `m.texttimer.ObserveField("fire", m.port)`
 
 This second case is used when you want a field change to trigger an event in a BrightScript message loop. This is useful when using BrightScript components (such as roChannelStore) which can only be instantiated in the main BrightScript thread or a Task node thread.