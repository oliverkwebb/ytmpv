# ytmpv - A dmenu based shell script for loading URL's with mpv
--------
## Default Requirements
- `yt-dlp` (https://github.com/yt-dlp/yt-dlp)
- `dmenu`
- `mpv`
- `ytfzf` (for "SADA")
- `notify-send` (change to `true` if you want notifications to be disabled)

## Actions
Special actions can be specified by putting `FOOBAR::` at the start of the URL.
For example `DOWN::https://www.foo.bar` will download the video located at `https://www.foo.bar`
The default action when no other action is specified is to play the URL given in `mpv`.

### List of Default Actions
- `DOWN` Downloads video with `yt-dlp` instead of playing it
- `XAUD` E**x**tract **Aud**io, Downloads video with `yt-dlp` with flags passed to yt-dlp
to extract only audio in Vorbis format, It will propmt for a name using `dmenu`
and only start downloading after the name is given, Downloads default to the "$HOME/Music"
Directory.
- `SADA` Runs `ytfzf` on prompt, Preforms the XAUD action on the URL of the selected video

## Configuration
Configuration can be done by changing the variables at the start of the code
For example, the video player is set in the `VIDP` variable at the start of the code

Refer to the source code and the docuentation for specified applications for
further configuration
