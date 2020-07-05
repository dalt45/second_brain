# [[Architectural Overview]]

![[Pasted image.png]]

[[BrightScript]] applications are dynamically loaded at runtime and run within a unique context within the BrightScript virtual machine. They are "sand-boxed" and run protected from other areas of the system. 

## User interface elements/Object model

The objects in the Roku SDK are divided into two primary areas:

- [[Core Objects]]: Fundamental objects that exist on all Roku platforms and are device independent
- [[Platform Objects]]: Objects unique to a specific platform, such as the Roku Streaming Player

Developing an application for the Roku Streaming Player consists of writing a [[BrightScript]] application, packaging the application and associated resource files and deploying it to the platform.

[[UI]] functionality available in the [[SDK]] includes:
- Top-Level Menu (Launch screen for applications with logo art)
- Poster Screen (Horizontally scrolling list of shows with poster art)
- Springboard (Detail screen with options for displaying individual shows)
- Video Player Screen (Video playback support with progress bar and trick mode support)
- PIN Entry Screen (User entry of PIN for purchase/rental verification)
 -Message/Error Dialog (Dialog for display of errors and other user messages)
- Filter Widget (Selection widget for filtering content display by type)
- Rendezvous/Code Registration Screen (Display/validate registration codes)
- Username/Password Registration Screen
- Text Screen ( Display formatted text to the user and allow selection of options)
- Search Screen (Keyword based search with progressive disclosure of results)

## Display Modes
The user interface has been designed to support both High Definition ([[HD]]) and Standard Definition ([[SD]]) displays.