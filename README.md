# ytmpv - A dmenu based shell script for loading URL's with mpv, yt-dlp, and ytfzf
--------

![Showcase](./showcase.gif)

## Why does ytmpv exist?
This project was created in reaction to Youtube and it's parent company Google
declaring war on adblock, removing my access to YouTube. Since I refuse to give YouTube
or Google money via Ad Revenue, I created this script to provide a quick access to proxies,
mainly yt-dlp. 

## Requirements
- `yt-dlp` (https://github.com/yt-dlp/yt-dlp)
- `dmenu` (ytfzf support will NOT work with the case insensitive patch, as it uses -i)
- `mpv`
- `ytfzf` (for Search Result Scraping)
- `notify-send`

## How to get audio from youtube videos using ytmpv
- Run `ytmpv -a SADA`, `ytmpv -a XAUD`, or `ytmpv`
- If you haven't already specified the action as `XAUD` or `SADA` specify either action by typing "XAUD::" or "SADA::"
before your URL or search term.
- If your specified action is `XAUD` provide the URL to the video you wish to download. If it is "SADA", provide a search term.
- If you have specified a search term, you will be prompted with the search results for that term, Select one.
- You will be asked for a subdirectory of `~/Music` to save the file in, if you do not chose one, it will be placed in `~/Music/`
- You will be asked for a filename, ".ogg" will automatically be appended to the end of the filename. If you do not choose a filename, it will be saved to "Song".
- The video will be downloaded, audio extracted, and you will be notified (unless -q is given) when the audio is done downloading, automatically saved to vorbis
format.

## How to browse and play Youtube videos with ymtpv
- Run `ytmpv -a SAP`, or `ytmpv`
- If you haven't already specified the action as `SAP` specify it by typing "SAP::" before your search term.
- If you have specified a search term, you will be prompted with the search results for that term, Select one.
- The video will be played with mpv; You will be notified (unless -q is given) if the video has failed to play

## Actions
Special actions can be specified by putting `FOOBAR::` at the start of the URL.
For example `DOWN::https://www.foo.bar` will download the video located at `https://www.foo.bar`
The default action when no other action is specified is to play the URL given in `mpv`.

- `DOWN` Downloads video with `yt-dlp` instead of playing it
- `XAUD` E**x**tract **Aud**io, Downloads video with `yt-dlp` with flags passed to yt-dlp
to extract only audio in Vorbis format, It will prompt for a name using `dmenu`
and only start downloading after the name is given, Downloads default to the "$HOME/Music"
Directory.
- `SADA` Runs `ytfzf` on prompt, Preforms the XAUD action on the URL of the selected video
- `SAP` Runs `ytfzf` on prompt, Preforms the PLAY action on the URL of the selected video

## Configuration
Configuration can be done by changing the variables at the start of the code
For example, the video player is set in the `VIDP` variable at the start of the code

Refer to the source code and the docuentation for specified applications for
further configuration
