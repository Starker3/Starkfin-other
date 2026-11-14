# Starkfin-other

A [Jellyfin](https://jellyfin.org) client for Samsung TVs. It's built on [litefin](https://github.com/MoazSalem/litefin) by Moaz Talaat, and it looks and works like Starkfin, a Jellyfin app for Apple TV. On the TV it's called **Starkfin**.

This repository has two things:
- **Update files:** the signed files the app downloads to update itself, served from GitHub Pages under `updates/`.
- **Source code:** each [release](https://github.com/Starker3/Starkfin-other/releases) has an archive of the code it was built from.

Development happens elsewhere, and this repository takes neither issues nor pull requests.

## What it adds to litefin

- **The Starkfin look:**
  - Home, title pages, Settings and pop-ups laid out like the Apple TV app.
  - A side menu.
  - Full-width hero artwork.
- **Profiles:**
  - A "Who's Watching" screen.
  - Optional PINs.
  - Full and Restricted profiles. A Restricted profile only sees titles at or under its rating limit.
- **Requests:** discover titles and request them through Seerr (Jellyseerr or Overseerr). This goes through the [Jellyfin Enhanced](https://github.com/n00bcodr/Jellyfin-Enhanced) plugin, so the app needs only your Jellyfin sign-in.
- **Search:** library search.
- **The player:**
  - A long-press menu on posters.
  - Remembers the quality you last picked.
  - A notice when the stream stalls on a slow connection.
  - Subtitles come back on when you skip back.
- **Updates inside the app:** covered in the next section.

Everything else, including playback, subtitles, Live TV, music and the plugins, is litefin's. Its [README](https://github.com/MoazSalem/litefin#readme) lists all of it.

## Updates

The app checks this site for new versions. You can change how it updates under **Settings › Updates**.

- **Channel:**
  - **Stable** gets releases that have passed testing.
  - **Test** also gets newer builds before they're ready.
- **Automatic updates:**
  - On: a new version downloads in the background and starts the next time the app opens.
  - Off: use **Check now**.
- **Older versions:** go back to a recent release, or to the version that came with the install.

Each update has a list of its files, signed with Ed25519. The app checks the signature and every file's SHA-256 fingerprint before it uses anything. If an update fails to start, the app goes back to the version it was using before.

Only Samsung TVs get updates for now.

## Installing

Neither the Samsung nor the LG store has the app. To install it:
1. Build the source from a release.
2. Sign the package with your own Samsung certificate. You make it in Tizen Studio for your TV.
3. Install it on the TV in Developer Mode.

Once installed, it keeps itself up to date from this site.

Testing has been on a Samsung TV running Tizen 6.0. The litefin build for other devices (LG webOS, Android TV, desktop) is in the source, but it hasn't been tested as Starkfin-other.

## Licence

Starkfin-other is licensed under the [Mozilla Public License 2.0](https://www.mozilla.org/MPL/2.0/), like litefin.

The fonts and libraries it bundles keep their own licences, which are listed in the app under **Settings › Open-source licences** and in each source archive.

Jellyfin is a trademark of the Jellyfin project. This app isn't affiliated with Jellyfin, Samsung or litefin.
