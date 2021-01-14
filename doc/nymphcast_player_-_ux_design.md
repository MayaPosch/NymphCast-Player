# NymphCast Player - UX Design #


## 0. Overview ##

This document covers the UX (user interaction) design behind the NymphCast Player (NCP). NCP is a client application that allows for interaction with other components of the NymphCast ecosystem, specifically the receiver devices (NymphCast Server, or NCS) and NymphCast MediaServer (NCMS).

A number of usage scenarios exist for end-users of NPC, which this document attempts to cover, along with desirable interaction patterns.

## 1. Usage patterns ##

The central goal with NCP for the end-user is the consumption of media, i.e. the starting of media playback (audio or audiovisual), on either a single NCS or a group of NCS devices. 

The source of this media content can be local files, media files made available by the NCMS, or media content offered by (third-party) NymphCast apps (NC apps).

## 2. Basic UX ##

The basic UX patterns are:

- Select local media file for playback on NCS device.
- Select media on NCMS for playback on NCS device.
- Select media in NC app for playback on NCS device.


All interactions have the same starting point: the NCP application. After this the focus diverges:

- Local media.
- Remote media.
- NC apps.

**2.1. Local media playback**

There are two obvious paths when it comes to playing back local media:

- Selecting a remote device to play back on.
- Selecting media to play back on a remote device.

If the main interface being presented to the user is that of the available devices (NCS) and media (local & NCMS), then both are valid paths.


**2.2. Remote media playback**

NCMS instances on the local network make a listing of media files available which can be selected for playback on target NCS devices.

The paths here are similar as for local media playback, highlighting the importance of presenting the available media in a manner that does not clutter the UI.

**2.3. NC app playback**

NC apps are a special case here. NC apps can be started from within NCP, but similar functionality may also exist in dedicated apps (using the same app-specific communication). Assuming the app is started from within NCP, this necessarily implies that first a target NCS device has to be selected within NCP, as said NC apps are provided by (i.e. run on) NCS devices.

This adds the requirement for:

- Starting an NC app on a target NCS device.
- Providing a UI for the NC app's graphical content.
- Providing a way to easily switch between NC apps, across NCS devices.