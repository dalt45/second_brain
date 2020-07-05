# Entry Points

There are several reserved function names that serve as entry points to the channel.

### Sub RunUserInterface()
#### Sub RunUserInterface(aa as Object)

RunUserInterface is the normal entry point which is called when a channel is selected on the Roku Home Screen. It may take an roAssociativeArray parameter that is passed via the External Control APIs.

### Sub Main()
#### Sub Main(aa as Object)
If there is no RunUserInterface() function in the application, the function Main() will be called as the entry point for the application.


### "Source" parameter

Its value represents the path the channel was launched from.

| Value of "Source"                                  | Launched from                                                          |
| -------------------------------------------------- | ---------------------------------------------------------------------- |
| "homescreen"                                       | "home" section of the main Roku channel selection page                 |
| "homescreen-menu"<br>_Available since Roku OS 9.3_ | Launched from a left-hand menu other than Featured Free or Roku Search |
| "ad"                                               | ad displayed to the right of the channels on the home page             |
| "external-control"                                 | [[ECP protocol]] (typically from the [[Deep Link]] tester or Roku mobile app)  |
| "partner-button"                                   | partner button on the Roku remote                                      |
| "other-channel"                                    | another channel on the Roku device                                     |
| "auto-run-dev"                                     | sideloaded developer channel                                           |
| "debug-server"                                     | debug server on port 8080.                                             |
| "purchase-dialog"                                  | Purchase dialog in the Channel Store                                   |
| "hs-search"                                        | Roku Search                                                            |
| "dial"                                             | [[DIAL protocol]]                                                          |
| "hs-d"                                             | launched from Feature Free page                                        |
| "my-feed"                                          | launched from My Feed page                                             |

### "lastExitOrTerminationReason" parameter

PluginEnums.h defines an ExitCode enum with a set of defined exit code reasons.

| Value of "lastExitOrTerminationReason" | Meaning                                                                                                                                                                                                                                                                                                                                                                           |
| -------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| EXIT\_UNKNOWN                          | Currently used as the default exit reason; either if there was no prior exit (i.e. first launch of the channel after system boot), or if there was no "unusual" exit reason noted (i.e. not due to a BrightScript crash or system resources issue).Used if the channel was exited by the system due to the device being powered off by the user (or by user-scheduled power off). |
| EXIT\_POWER\_MODE                      | Used if the channel was exited by the system due to the device being powered off by the user (or by user-scheduled power off).                                                                                                                                                                                                                                                    |
| EXIT\_DIAL\_DELETE                     | Used when a DIAL-controlled channel exits due to a command received from the second screen app to exit the channel.                                                                                                                                                                                                                                                               |
| EXIT\_OUT\_OF\_MEMORY                  | Used if a channel exits due to the system being under low memory conditions.                                                                                                                                                                                                                                                                                                      |
| EXIT\_IDLE\_AUTO\_EXIT                 | Used if the system and channel were detected as idle for a prolonged period of time and the system exits the channel per Roku policy.<br><br>_Available since Roku OS 8.1_                                                                                                                                                                                                        |
| EXIT\_BRIGHTSCRIPT\_CRASH              | Used if a BrightScript runtime error caused the channel to exit.<br><br>_Available since Roku OS 8.1_                                                                                                                                                                                                                                                                             |
| EXIT\_BRIGHTSCRIPT\_STOP               | Used if a BrightScript 'stop' command was encountered when running the channel in production mode (non-developer sideloaded). This is treated by the system the same as a BrightScript runtime error and the channel exits.<br><br>_Available since Roku OS 8.1_                                                                                                                  |
| EXIT\_BRIGHTSCRIPT\_TIMEOUT            | Used if a BrightScript execution timeout error occurred and the channel exits. (A timeout error occurs indicates that the channel user interface was unresponsive for a prolonged period of time, such as program lock-up).<br><br>_Available since Roku OS 8.1_                                                                                                                  |

### Sub RunScreenSaver()
RunScreenSaver is called to launch a screensaver when the Roku has been idle for the configured idle time.

### Sub RunScreenSaver()

RunScreenSaverSettings is called when the user selects “Custom Settings” on the Screensaver settings page.

### User interaction/events

Roku SDK UI objects provide an event oriented model for user interaction. Instead of receiving and directly handling all of the IR events received by the application, the UI elements will handle all navigation commands directly and send higher level events to the script as the focus changes or the user makes a selection.

> As Luis pointed these events are received in the component itself and they can be addressed in a function which returning a "true" value will prevent the propagation to the parents (bubbling).

### Customization 

The objects in the user interface framework expose a set of [[screen types]] which standardize user interaction and make it easy for developers to quickly write and deploy applications. 