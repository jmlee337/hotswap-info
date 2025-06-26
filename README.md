# Table of Contents
- [The Story of Hotswap](#the-story-of-hotswap)
- [Getting Started](#getting-started)
- [Applications of Per-Set Replays](#applications-of-per-set-replays)
- [Other Related Tools](#other-related-tools)

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

<img width="613" alt="Screenshot 2025-06-25 at 12 41 25" src="https://github.com/user-attachments/assets/163d07b6-40ad-4cec-8348-a5fde29a8656" />

# Getting Started
To start producing *Per-Set Replays* you will need the following:

- [Slippi Nintendont](https://github.com/project-slippi/Nintendont/releases/latest) -
At time of writing, the latest version to contain hotswap improvments is `v1.13.0` from April 2025.
If your Wiis are only used for tournament Melee, I recommend setting them up to fully autoboot to CSS.
- [Replay Manager for Slippi](https://github.com/jmlee337/replay-manager-for-slippi/releases/latest) -
Used to simultaneously group, label, and package *Per-Set Replays* while reporting set results to start.gg (or Challonge).
Can be operated by a TO and/or set to walkthrough mode for player self-service.
Available for Windows, Mac, and Linux.
- USB Drives - USB 2.0 or later required.
A tournament replay takes up about 1 MB per minute, so even a 1 GB drive is bigger than you could ever possibly need.
I've found it's possible to get small USB 2.0 drives used or surplus for as low as $1 each.
A new drive seems to cost at least $3 each from the likes of Microcenter.

In tournament the hotswap workflow looks like this:

1. The players take and insert a USB drive before starting their set
2. The players play their set as normal
3. The players return the USB drive to the TO when reporting their result.
4. The TO uses Replay Manager for Slippi to turn the replays from the returned USB drive into *Per-Set Replays* and report the result to start.gg.

# Applications of Per-Set Replays
- Auto VODs
- Auto Stream
- Melee Improover
- Rwing

# Other Related Tools
- start.gg VOD Assigner
