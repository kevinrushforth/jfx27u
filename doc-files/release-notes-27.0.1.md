# Release Notes for JavaFX 27.0.1

## Introduction

The following notes describe important changes and information about this release. In some cases, the descriptions provide links to additional detailed information about an issue or a change.

These notes document the JavaFX 27.0.1 update release. As such, they complement the [JavaFX 27](https://github.com/openjdk/jfx27u/blob/master/doc-files/release-notes-27.md) release notes.

## Important Changes

### JavaFX: Deserialization of Object Graphs from the Clipboard Is Disabled by Default

Deserialization of object graphs is disabled by default when reading data from the clipboard or during drag-and-drop operations. For a custom `DataFormat`, a directly serialized `String` is decoded by default; other serialized objects are returned as a `ByteBuffer`.

Applications can restore the previous ability to deserialize arbitrary object graphs by setting the `javafx.dnd.deserializeObjectGraph` system property to `true`.

## List of Fixed Bugs

Issue Key | Summary | Subcomponent
--------- | ------- | ------------
[JDK-8389515](https://bugs.openjdk.org/browse/JDK-8389515) | Memory leak in dshowwrapper - decoded buffers delivered by CSink are never unmapped | media
[JDK-8380556](https://bugs.openjdk.org/browse/JDK-8380556) | Update WebKit to 625.1 | web
[JDK-8386859](https://bugs.openjdk.org/browse/JDK-8386859) | WebView crashes when calling document.startViewTransition() | web
[JDK-8388451](https://bugs.openjdk.org/browse/JDK-8388451) | Additional WebKit 625.1 fixes from WebKitGTK 2.52.5 | web
[JDK-8390652](https://bugs.openjdk.org/browse/JDK-8390652) | Additional WebKit 625.1 fixes from WebKitGTK 2.52.6 | web
[JDK-8391823](https://bugs.openjdk.org/browse/JDK-8391823) | Intermittent WebView crash when running TextureMapperTest | web
[JDK-8389783](https://bugs.openjdk.org/browse/JDK-8389783) | Crash in JavaFX native glass toolkit during Timer shutdown | window-toolkit

## List of Security fixes

Issue Key | Summary | Subcomponent
--------- | ------- | ------------
JDK-8383312 (not public) | Enhance JavaFX CSS Handling | controls
JDK-8383332 (not public) | Improve JavaFX Input Methods | controls
JDK-8383356 (not public) | Improve JavaFX Rich Text Formatting | controls
JDK-8388783 (not public) | Custom String data cannot be read from the clipboard after JDK-8383252 | controls
JDK-8383219 (not public) | Enhance JavaFX Document Loading | fxml
JDK-8383252 (not public) | Enhance JavaFX DnD | graphics
JDK-8383333 (not public) | Improve JavaFX Drag and Drop | graphics
JDK-8386486 (not public) | Improve graphics rendering | graphics
JDK-8389176 (not public) | Enhance JavaFX image handling | graphics
JDK-8391652 (not public) | Snapshot test failures after JDK-8389176 | graphics
JDK-8383209 (not public) | Improve JavaFX Scripting Support | web
JDK-8385198 (not public) | Enhance JavaFX Resource Loading | web
JDK-8383229 (not public) | Enhance JavaFX Image Loading | window-toolkit
JDK-8383322 (not public) | Enhance JavaFX Clipboard | window-toolkit
