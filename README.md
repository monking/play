# Pirate Radio

`play` some music, and stream it to your buddies.

## usage

`./play [playlist] [options] [mplayer options]`

`[playlist]` is a .m3u file in a `playlists/` directory next to the `play` script.

`[options]` are listed below. Any unknown options are assumed to be meant for `mplayer`.

## options

- `-eq-boom` - boost the 31.25-62.5 Hz range (big buttery bass)
- `-no-shuffle` - play the playlist in order
- `-enable-video` - if a file in a playlist has video, this will allow it to show
- `-say` - pipe a spoken message into Soundflower, thus the broadcast (excludes all other options)

## broadcast (currently Mac only)

- set soundflower 2ch to default input and output (System Preferences.app)
- run `./play playlist -broadcast`
- **if** you don't want your system sounds dumping into the radio broadcast
	- set default sound input/output back to the built-in

## examples

`./play hotline.m3u -eq-boom -volume 6`
- `-volume 6` will be passed through to `mplayer`

## installation

### Mac

- do `brew install mplayer jack darkice icecast` in the command line
- install [soundflower](https://rogueamoeba.com/freebies/soundflower/)

## caveats

This tool was created for personal use on a Mac running OS X 10.9.5. No testing
has been done on other systems, though the greater part of this setup should be
portable to other POSIX systems.
