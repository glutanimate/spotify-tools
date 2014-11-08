# Spotify™ Tools

A collection of bash scripts interfacing with Spotify on Linux.

## Table of contents

<!-- MarkdownTOC -->

- [Installation](#installation)
- [Scripts](#scripts)
    - [spotify_adjust_volume](#spotify_adjust_volume)
    - [spotify_announce_tracks](#spotify_announce_tracks)
    - [spotify_display_trackinfo](#spotify_display_trackinfo)
    - [spotify_save_track](#spotify_save_track)
- [License](#license)
- [Important notice](#important-notice)

<!-- /MarkdownTOC -->

## Installation


1. Check out the latest version of this repository either by downloading the `.zip` file or cloning the entire repo

2. Place the scripts folder in a location of your choice 

3. Install all the dependencies required by whatever script you plan to use (see below for a dependency list for each script)

4. Optional:

    4.1. move the scripts to your `PATH`

    4.2. set up key-bindings in your desktop environment of choice


## Scripts

### spotify_adjust_volume

**Overview**

A simple `xdotool` macro that controls Spotify volume from the command-line / a keyboard shortcut.

**Usage**

    spotify_adjust_volume Up|Down

*Note:* Might not work if Spotify is minimized.

**Dependencies**

    xdotool spotify

### spotify_announce_tracks

**Overview**

A script that sits in the background and announces Spotify track changes via [simple-google-tts](https://github.com/Glutanimate/simple-google-tts) (or any other text-to-speech software, for that matter).

**Usage**

    spotify_announce_tracks

*Note:* To use a different TTS application, modify the value of the `TTSEngine` variable in the script.

**Dependencies**

    xdotool x11-utils simple-google-tts spotify

### spotify_display_trackinfo

**Overview**

Shows a one-time notification containing track data and reads out the artist and title via text to speech.

**Usage**

    spotify_display_info

*Note:* To use a different TTS application, modify the value of the `TTSEngine` variable in the script.

**Dependencies**

    xdotool x11-utils libnotify-bin simple-google-tts spotify

### spotify_save_track

**Overview**

Xdotool macro that saves the active track to your Spotify collection or notifies you if it's already saved.

**Usage**

    spotify_save_track

*Notes:* 

- the script assumes that you have your album art preview set to the largest size possible. If that's not the case you will have to adjust the `CheckMarkX` and `CheckMarkY` values. Otherwise `xdotool` will "click" on the wrong part of the UI
- might not work if Spotify is minimized
- will temporarily change focus to Spotify when executed

**Dependencies**

    xdotool x11-utils libnotify-bin imagemagick

## License

*Spotify™ Tools copyright 2014 Glutanimate*

The scripts in this repository are licensed under the [GNU GPLv3](http://www.gnu.de/documents/gpl-3.0.en.html).

## Important notice

The products in this repository are not endorsed, certified or otherwise approved in any way by Spotify. Spotify is the registered trademark of the Spotify Group.