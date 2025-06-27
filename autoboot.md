# Full Autoboot
Full autoboot means powering on and walking away while the Wii boots all the way into Melee.
This is achieved by chaining *Priiloader Autoboot* together with *Slippi Nintendont Auto Boot*.
To set up full autoboot you will need:
- A Wii with Homebrew Channel installed.
- [Slippi Nintendont](https://github.com/project-slippi/Nintendont/releases/latest), `v1.13.0` (April 2025) or later.
This version included a fix for a bug that could cause launching Melee to get stuck on a black screen before reaching the game, preventing true walk-away workflows.
- Forwarder for Slippi Nintendont, which is included in the Slippi Nintendont download.
- [Priiloader](https://github.com/DacoTaco/priiloader/releases/latest), download the installer (at time of writing `Priiloader_v0_10.zip`).
If your installed Priiloader version is too old this won't work, so if you have problems try installing the latest version.
I once had problems with an installed Priiloader that was version `0.7` (April 2011) or earlier (it had a white background).
I suspect version `0.8` (July 2015) should work, please let me know if that is the case for you.

## Prerequisite: No BootMii-boot2
You may also need:
- [HackMii Installer](https://bootmii.org/download/) to uninstall BootMii-boot2.
If the Wii boots to this menu:
![image](https://github.com/user-attachments/assets/1e987a3e-9609-424f-a328-df5d40a007bc)
that means you have BootMii-boot2 installed.
BootMii-boot2 cannot be used in full autoboot and will interfere with *Priiloader Autoboot* unless specially configured.
The simplest thing to do is uninstall it by running HackMii Installer via Homebrew Channel.
> It's also possible for BootMii-boot2 to be configured to boot to Homebrew Channel **without** showing the menu pictured above.
If the Wii still boots to Homebrew Channel **after** changing Priiloader's `Autoboot` setting in the setup steps below, uninstall BootMii-boot2 by running HackMii Installer via Homebrew Channel.
## Setup
After running the Priiloader installer via Homebrew Channel, access Priiloader settings by holding the Wii RESET button while powering on.

Select `Load/Install File`:

![vlcsnap-2025-06-26-18h18m35s057](https://github.com/user-attachments/assets/9aaa041e-3ca5-4767-953c-bb6281b646fa)

Select `Forwarder for Slippi Nintendont`:

![vlcsnap-2025-06-26-18h18m45s323](https://github.com/user-attachments/assets/298ee81a-38cc-430a-8a07-55f4970e45e3)

Select `Settings`:

![vlcsnap-2025-06-26-18h18m53s536](https://github.com/user-attachments/assets/10945d58-4df4-4ec2-a9eb-efd652a718cb)

Change `Autoboot` to `Installed File`, then select `save settings`:

![vlcsnap-2025-06-26-18h19m03s840](https://github.com/user-attachments/assets/f00e9dc5-13eb-45d1-b519-5cb70e0c6204)


Hold the Wii POWER button until the console turns off, then turn it back on and verify that it boots to Slippi Nintendont.
> If the Wii boots to Homebrew Channel instead, even after double checking the previous steps, you have BootMii-boot2 installed.
Follow the above [Prerequisite: No BootMii-boot2](#prerequisite-no-bootmii-boot2) steps.

In Slippi Nintendont once all your `Slippi Settings` are set, press L or R to access the second page, `Nintendont Settings`.
Change `Auto Boot` to `On`:

![vlcsnap-2025-06-26-18h23m20s225](https://github.com/user-attachments/assets/80b9089e-2b3f-499c-a57f-d82b15900cf9)

Press B to return to the games list and launch Melee.
Full autoboot is now set up.
You can verify this by powering on and seeing that the Wii boots all the way into Melee with no input required.

Holding the Wii RESET button while powering on will still access Priiloader settings, interrupting *Priiloader Autoboot*.

*Slippi Nintendont Auto Boot* allows you to press B to cancel it during an onscreen prompt.
You can do this if you need to change `Slippi Settings`.
However, this changes Slippi Nintendont's `Auto Boot` setting to `Off` so be sure to turn it back on when you're ready. 
