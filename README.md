# Jasheroke for Android

<img width="1672" height="941" alt="ANDROID" src="https://github.com/user-attachments/assets/87042b51-978c-49b2-9c27-44a14a69ba0e" />

**Version 2.0.0** | StackSync Solutions

English | [Tagalog](README.tl.md)

Jasheroke turns an Android device into a karaoke player or a companion for reserving songs. Sing from your local library, host a reservation room, or join a Windows or Android host from your phone.

## Download

Download **Jasheroke.apk** from this repository's **Releases** section. To use a Windows PC as your karaoke host, download **Jasheroke.exe** for Windows.

| Application | Current version | Purpose |
| --- | --- | --- |
| Jasheroke for Android | 2.0.0 | Android karaoke player, reservation host and phone companion |
| Jasheroke for Windows | 1.3.0 | PC karaoke player and reservation host |

## Requirements

- **Android 8.0 or newer**.
- A compatible song library for local karaoke playback. A SoundFont is already bundled with the app.
- A shared local network or Wi-Fi connection when joining or hosting a reservation room.
- Microphone permission only when using microphone features.

The APK supports ARM and x86 devices, both 32-bit and 64-bit. Phone reservation mode needs no local song files or microphone permission.

## Features

- **Library:** search by title, artist or song number; play, reserve and favorite songs.
- **Phone:** join a host, search its catalog, reserve songs and view the live queue.
- **Room:** accept phone reservations, see singer names and manage playback and the queue.
- **Stage:** landscape karaoke with synchronized lyrics, video backgrounds and reserved song numbers visible at the top.
- **Settings:** dark, light or system appearance, library scanning, SoundFont selection, backgrounds and permissions.
- Key adjustment of ±6 semitones and tempo from 0.5× to 2×, remembered for each local song.
- Saved favorites and recovery of an interrupted reservation queue.

## Install the app

1. Download `Jasheroke.apk` onto the Android device.
2. Open the APK. If Android asks, allow installation from the browser or file manager used to open it.
3. Complete installation and open Jasheroke.
4. Open **Phone** to join a host, or configure your song library in **Settings** for local playback.

## Reserve songs on a Windows or Android host

1. Connect the host and phone to the same local network or Wi-Fi.
2. Start a room on the host. On Windows, use **Phones → Start room**. On Android, use **Room → Open reservation room**.
3. On your phone, open **Phone** and enter the host address, your singer name and the six-digit PIN displayed by the host.
4. Search for a song and select **Reserve**.
5. Open **Live queue** to follow the current song and waiting reservations.

An address may look like `192.168.1.20:17890`. The phone searches the host's library, so song files stay on the host. You can cancel your own waiting reservations; the host manages playback, skipping and queue order.

Keep the host app running. For an Android host, keep the app in the foreground during the karaoke session. Restarting the room requires guests to join again.

## Play karaoke on Android

1. Copy a compatible song library to the device, keeping the matching files in the same folder.
2. Open **Settings**, use **Library access** to grant access when needed, and select the song folder.
3. Select **Save & scan**, then open **Library** to choose a song.
4. Play immediately or reserve the song. Use **Room** to manage the queue.

| Library format | Files needed |
| --- | --- |
| Indexed library | `jashidx` and `jashblob` |
| Paired library | `lyrics.jash` and `mid.jash` |

Song libraries and background videos are supplied separately. Use the bundled SoundFont or configure another `.sf2` file or folder in Settings. Select a background video folder if desired.

To use a microphone, select **Enable microphone** in Settings and grant permission. Headphones help reduce feedback when monitoring your voice.

## Host a reservation room

Prepare the Android host's local library first, then select **Room → Open reservation room**. Share the displayed address and PIN with singers. Other Android devices can join through their **Phone** tab.

Rooms use port **17890**. Devices must be able to reach one another on the network. Guest Wi-Fi with device isolation may prevent connections. Windows hosts may need permission through Windows Firewall on the private network.

## Recover a session

After a saved queue is recovered, review it and choose to resume. An interrupted song returns to the front and restarts from the beginning. Playback waits for your action.

## Update the app

Install a newer release over the existing app to retain settings when Android accepts the update. If an older debug installation has a conflicting signing certificate, uninstall that installation before installing the release. Uninstalling clears app-private settings and reservations, so preserve anything you need first.

## Troubleshooting

| Problem | What to check |
| --- | --- |
| Phone cannot connect | Check the address, PIN, shared network and host status. Rejoin after a room restart. |
| Library is empty | Check library access, folder selection and matching library files, then scan again. |
| MIDI playback is silent | Check the SoundFont selection, media volume and audio output. |
| Microphone is unavailable | Grant microphone permission in Settings and check the audio route. |
| Android rejects an update | Check for an older debug installation with a different signing certificate. |

## Report an issue

Use this repository's **Issues** section. Include the app version, device model, Android version, steps to reproduce the problem and any error message. For reservation problems, include the host platform and app version.

Developed by **StackSync Solutions**.
