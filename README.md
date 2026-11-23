# PENDING - Carplay-Advanced-Installer. Identical to NBT EVO APK Originally Developed by @BimmerTuner. Fully Redesigned from bits of code by @ghackt with many additional features But for Carplay Gauge / HUD Navigation Capabilities side for ID5 and ID6. This is not Android Auto Installer. This can work along side Android Auto tweak.

First of all thank you all for giving me a shot and my files. If you encounter any issues 
PLEASE OPEN A TICKET https://github.com/ghackt/Carplay-advanced-installer/issues/new

## Donations or Coffee Giving.

The application and updates are totally free. I make absolutely nothing from this. If you are feeling generous any small amount helps and links for donations are below but its not required from you.

 - Been Tired of all these companies charging outrageous prices for other people’s work. Also been tired of these Chinese companies forcing people to buy MMI boxes and taking advantage of us all.
 
<link>https://www.paypal.me/JamieBland371</link>

<link>https://www.venmo.com/ItsJamesB</link>
 
or @ItsJamesB in the venmo app search.


<img width="1206" height="880" alt="IMG_4488" src="https://github.com/user-attachments/assets/63d0d81f-be19-4f0c-a967-fed3e2ceee84" />
<img width="5712" height="4284" alt="IMG_4478" src="https://github.com/user-attachments/assets/86b581c7-0184-4280-9d90-d2d12e09d181" />
<img width="4284" height="5712" alt="IMG_4483" src="https://github.com/user-attachments/assets/29c190d7-90f9-4dd4-9872-16484c7fd069" />
<img width="4284" height="5712" alt="IMG_4485" src="https://github.com/user-attachments/assets/6e45b9f1-9bd6-442a-8fca-8f155e095d26" />
<img width="4284" height="5712" alt="IMG_4484" src="https://github.com/user-attachments/assets/cf7ebf08-760f-4d72-98b5-b1a4aafd8690" />
<img width="4284" height="5712" alt="IMG_4487" src="https://github.com/user-attachments/assets/29448410-a0fe-45c1-a91d-b6e6a4bd8a68" />


An easy AIO installer for those who have issues using SSH and installing things manually like I do sometimes.

I built a Windows version of the installer from the app's files. An Android APK can't run on Windows, so this is a new Windows program written from the 1.6.7 source that does the same job over a wired ENET cable from your laptop. Nothing has been tested on a real PC or car yet, so try it carefully on a car you own.

What's in the zip:

CarPlayAdvancedInstaller.exe (64-bit) and CarPlayAdvancedInstaller-arm64.exe (ARM PCs).
README.txt with step-by-step instructions.
source/ the full source code and a BUILD.md.

How it works: you double-click the .exe, a small window opens, and your browser opens the app at a local 127.0.0.1 address. Everything runs on your own PC. The screens mirror the phone app, dark theme and all: the animated welcome, Step 01 connect, Step 02 release list with scrolling notes, install/uninstall/restart, the credits, the coffee links, the red notice, and the log with the summary header.

What I carried over from the phone app, faithfully:

SSH unlock through the same third-party relay (wss://pretzel.bavarian-aa.uk:8443), including the exact three-frame handshake, the 0x81/0x82/0x83 relay frames, the gateway bridge on TCP 6801, and the safety block on the dangerous UDS routine.
Gateway discovery by BMW ENET identification broadcast, with manual gateway entry as a fallback.
Head-unit SSH, the on -f /net/hu-omap/ command wrapper, and hash-verified file uploads.
The supported-software table, all four builds including Build 29 (any CarPlay library) and Build 41 (with the mm-ipod check), plus HUD-only fallback.
Release catalogue from Ghackt and st1ng on GitHub, the two bundled payloads, download, and install.

What I tested here: the WebSocket framing, the relay frame decoder, the handshake bytes, the safety guard, the hash table, offline building, and the local server (it loads all 53 releases live from GitHub). I could not test the actual car-side SSH unlock or install, since that needs a head unit.

Two things to know:

The .exe isn't code-signed, so Windows SmartScreen will warn ("More info → Run anyway"), and you'll get a firewall prompt for the local page.
The release you install must list your head-unit build, or its installer stops with "Unknown software" before changing anything.

The file is /mnt/user-data/outputs/CarPlayAdvancedInstaller_Windows.zip.

## License

The bundled nbtevo-carplay-advanced files are under the **PolyForm Noncommercial 1.0.0** license: personal/hobby use only, no selling or commercial use. Copies of its LICENSE and NOTICE are in [`licenses/`](licenses/).
I have not verified the license of the original app; rights in it remain with its authors.

