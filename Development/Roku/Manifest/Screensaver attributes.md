# Screensaver attributes

| Attribute           | Type    | Description                                   | Sample manifest entry               |
| ------------------- | ------- | --------------------------------------------- | ----------------------------------- |
| `screensaver_title` | string  | name of the screensaver displayed in Settings | `screensaver_title=Dog Screensaver` |
| `major_version`     | integer | major portion of the screensaver version      | `major_version=1`                   |
| `minor_version`     | integer | minor portion of the screensaver version      | `minor_version=2`                   |
| `build_version`     | integer | build number                                  | `build_version=150`                 |

### Optional screensaver attributes


| Attribute             | Type    | Description                                                             | Sample manifest entry   |
| --------------------- | ------- | ----------------------------------------------------------------------- | ----------------------- |
| `screensaver_private` | integer | Attribute to specify if the screensaver will only run within a channel. | `screensaver_private=1` |
