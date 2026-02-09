# Table of Contents
- [The Story of Hotswap](#the-story-of-hotswap)
- [Getting Started](#getting-started)
- [Applications of Per-Set Replays](#applications-of-per-set-replays)
- [Frequently Asked Questions (FAQs)](#frequently-asked-questions-faqs)

# The Story of Hotswap
In the beginning there was the Slippi replay.
This perfect digital representation of a game of Melee became the basis of modern netplay and production, but consoles did not see the same benefits at first.
A few TOs diligently uploaded full dumps, hundreds of files at a time, amounting to gigabytes of replays rarely touched.
Only the most dedicated preservationists and players attempted to sort through these vast archives, winnowing out handwarmers and friendlies, searching for the right nametag or port or character or color.
And all that only to review a set on PC or maybe record a clip to post to Twitter.

However, there is now a better way.

The shortcoming of Slippi replays is that they work **per-game**, while much of console Melee is played **per-set**.
Now, USB hotswap in Slippi Nintendont makes it practical to collect replays per-set.
With Replay Manager for Slippi we can add player names, scores, and information about the set all while reporting the result to start.gg in the same amount of time.
The result is replays grouped and labelled by set, packaged together with all relevant context, henceforth referred to as *Per-Set Replays*.

<img width="778" alt="Screenshot 2025-06-25 at 12 17 38" src="https://github.com/user-attachments/assets/35e11d74-2eb9-4573-98c2-a4677c5a9d23" />

While the emergence of replay-based practice tools makes this great for players, it's also great for TOs.
Aside from the hotswap workflow inherently putting character, game, and stage data in start.gg, *Per-Set Replays* can also be used for Auto VODs and Auto Streams.
This is the bracket your bracket could look like:

[<img width="613" alt="Front Runners #30" src="https://github.com/user-attachments/assets/163d07b6-40ad-4cec-8348-a5fde29a8656" />](https://www.start.gg/tournament/front-runners-30/event/melee-singles/brackets/1984102/2910341)

# Getting Started
To start producing *Per-Set Replays* you will need the following:

- [Slippi Nintendont](https://github.com/project-slippi/Nintendont/releases/latest) -
At time of writing, the latest version to contain hotswap improvments is `v1.13.0` (April 2025).
If your Wiis are only used for tournament Melee, I recommend setting up [full autoboot](autoboot.md).
- [Replay Manager for Slippi](https://github.com/jmlee337/replay-manager-for-slippi/releases/latest) -
Used to simultaneously group, label, and package *Per-Set Replays* while reporting set results to start.gg (or Challonge).
Can be operated by a TO and/or set to walkthrough mode for player self-service.
Available for Windows, Mac, and Linux.
- USB Drives - USB 2.0 or later required.
I recommend formatting your USB drives as exFAT (as opposed to FAT32 - if booting P+ as well see [this guide](projectplusgame.md)).
A tournament replay takes up about 1 MB per minute, so even a 1 GB drive is bigger than you could ever possibly need.
I've found it's possible to get small USB 2.0 drives used or surplus for as low as $1 each.
Of course there is some risk of ending up with low-quality drives this way.
A new drive seems to cost at least $3 each from the likes of Microcenter.

In tournament the hotswap workflow looks like this:

1. The players take and insert a USB drive in the Wii (either port) before starting their set.
2. The players confirm that the disc drive lights up and remains solid blue: this means that replays are working.
3. The players play their set as normal.
4. The players return the USB drive to the TO when reporting their result.
5. The TO uses Replay Manager for Slippi to turn the replays from the returned USB drive into *Per-Set Replays* and report the result to start.gg.

# Applications of *Per-Set Replays*
*Per-Set Replays* are more convienent for TOs to upload since when the bracket ends they're already all in one place.
They are also more convenient for players to download, making it easier to use tools like [Melee Improover](https://github.com/Fiction52s/Melee-Improover/releases/latest), [rwing](https://www.patreon.com/rwing_aitch), and [Project Clippi](https://github.com/vinceau/project-clippi/releases/latest).
*Per-Set Replays* are compressed by default which makes them easier on TO's cloud storage limits.
Perhaps most importantly, there are also tools which specifically use *Per-Set Replays*, enabling TOs to do new things with very little effort:
- [Auto VODs](https://github.com/davisdude/slp2mp4/releases/latest) -
slp2mp4 by GrayCode turns *Per-Set Replays* into videos ready to be uploaded to YouTube.
It is fully walk-away automatic, no OBS required or anything like that.
Best used for **larger** tournaments that happen less frequently, like monthlies, regionals, etc.
  - [ingest_startgg.py](https://github.com/jmlee337/replay-viewer/blob/normalize/scripts/ingest_startgg.py) can be used to attached the resulting VODs to start.gg.
- [Auto Stream](https://github.com/jmlee337/auto-slp-player/releases/latest) -
Auto SLP Player enables the TO operating Replay Manager to run an auto-quad stream from the same PC.
Of course, the PC must be able to run 4 Slippi Dolphins at the same time.
Best used for **smaller** tournaments that happen more frequently, like weeklies.
Auto SLP Player produces timestamps for every set so the VOD can be easily browsed by players and viewers.
By streaming to Twitch and YouTube using [Restream](https://restream.io), the TO can produce a YouTube Live VOD complete with timestamps shortly **before** bracket ends.
  - Auto SLP Player produces timestamps for every set so the VOD can be easily browsed by players and viewers.
    It can attach VOD links to start.gg as well.

# Other Helpful Tools
- [Auto Config for Slippi](https://github.com/jmlee337/auto-config-for-slippi/releases/latest) -
lets you easily make sure all your SD cards have the same version of Slippi Nintendont and the same settings.
- [Offline Mode for start.gg](https://github.com/jmlee337/local-cache-for-startgg/releases/latest) -
is an offline client for start.gg which protects your tournament from outages, whether on your end or theirs.
It can be used with Replay Manager or standalone.
- [Wii Network Config Editor](https://github.com/Bazmoc/Wii-Network-Config-Editor/releases/latest) -
can be used to set your Wiis' network without a wiimote or internet connection.


# Frequently Asked Questions (FAQs)
## Can I record to 2 USB drives at once?
No.
## Will using the hotswap workflow slow down my bracket?
Within reason, no.
In practice, for a pool up to 64 players one TO operating Replay Manager can be fast enough to avoid any line forming.
If you have more than 64 players per wave, you should expect to need extra laptops and TOs.
Some TOs attest that reporting through Replay Manager is **faster** than start.gg's website.
## Why not FAT32?
For some reason, Slippi Nintendont struggles and often fails to write to FAT32 drives that are more than about 50% full.
If you need to boot P+ off the same USB drives used for hotswap, see [this guide](projectplusgame.md)).
