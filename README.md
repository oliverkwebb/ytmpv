# ytmpv - A dmenu based shell script for loading URL's with mpv
--------
## Default Requirements
- `[yt-dlp](https://github.com/yt-dlp/yt-dlp)`
- `dmenu` (It is recommenced that you change the dmenu source code to remap pasting to C-V)
- `mpv`
- `notify-send` (change to `true` if you want notifications to be disabled)

## Actions
Special actions can be specified by putting `\[FOO\]::` at the start of the URL.
For example `DOWN::https://www.foo.bar` will download the video located at `https://www.foo.bar`
The default action when no other action is specified is to play the URL given in `mpv`.

### List of Default Actions
- `DOWN` Downloads video with `yt-dlp` instead of playing it
- `XAUD` E**x**tract **Aud**io, Downloads video with `yt-dlp` with flags to extract only audio in Vorbis format

## Configuration
Configuration can be done by changing the variables at the start of the code
For example, the video player is set in the `VIDP` variable at the start of the code

Refer to the source code and the documentation for specified applications for further configuration
