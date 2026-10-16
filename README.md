# Edrys Station-Stream Module

> [!WARNING]
> **Deprecated.** This module is superseded by
> [module-streaming](https://github.com/edrys-labs/module-streaming), which has the same settings and camera picker,
> and adds stream quality, several streams per station (`streamName`), a websocket relay for networks that block
> peer-to-peer, and automatic recovery when the camera is lost. This module only gets critical fixes.
>
> **Switching:** add `https://edrys-labs.github.io/module-streaming/index.html` instead. `video`, `audio`, `mirrorX`,
> `mirrorY` and `rotate` keep their names.
>
> - `audio` is **off by default** there: set it to `true` (or tick it in the settings form) to keep streaming the microphone.

This module will allow a station to send a video and or audio stream to all connected users via a direct WebRTC connection.

Import the module via:

`https://edrys-labs.github.io/module-station-stream/index.html`

## Settings

By default, the station will share the video and audio signal from a connected webcam.
You can tweak this behavior with the following settings for station-mode:

``` yaml
video: true
audio: false
mirrorX: false
mirrorY: true
rotate: 90
```

or via json:

``` json
{
    "video": true,
    "audio": false
}
```

The flip parameters will flip the video horizontally or vertically.

## Problems

It is recommended to use Chrome in station mode. Firefox might have some restrictions, but any browser with WebRTC support should support the client-side viewing.
