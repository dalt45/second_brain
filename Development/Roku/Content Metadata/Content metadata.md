
# Content Metadata
Content metadata describes a viewable title that will be shown to the user. Content may be any supported type of video and the metadata is used by the UI to format and display the title to the user. Some attributes (e.g. ContentType) affect how the title is displayed on screen, other attributes (e.g. SDPosterURL) specify where to fetch artwork to display with the content and other attributes (e.g. Title) are just rendered as text.

- Stored in an associative array
- Provided to various [[Screen Objects]] as need for display
- An array of [[Content metadata]] can be provided to be rendered as a list
- Certain attributes are recognized by particular screens

Theres **two ways** to specify [[Content metadata]] **[[data.Stream]]** and **[[data.Streams]]**

- [[data.Stream]]: This is used when there is one stream URL, typically an HLS or smooth streaming manifest URL.
- [[data.Streams]]: This is used when you have a set of fixed bitrate streams. This is typically the case for non-adaptive MP4 streams, in which case multiple variants are specified to simulate true adaptation.

### 1. [[Descriptive attributes ]]
### 2. [[DRM attributes]]
### 3. [[Playback configuration attributes]]
### 4. [[CDN switching attributes]]
### 5. [[SceneGraph cerificate attributes]]
### 5. [[Playback control attributes]]
### 6. [[Track ID attributes]]
### 7. [[roListScreen attributes]]
### 8. [[roImageCanvas attributes]]
### 9. [[TextAttrs attribute keys]]
### 10. [[Rating attribute icons]]


