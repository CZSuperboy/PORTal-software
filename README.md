# PORTal-software
## SD Card image for my raspberry pi 4-based portable gaming device, the PORTal
**DISCLAIMER**

All software contained within this image that is not my own belongs to their respective companies and teams. I am not directly affiliated with said companies/teams in any way, and this software is not being rereleased for personal gain or profit.

###**HOW TO INSTALL** (Pictures coming soon)

The image is released as a standard raspberry pi SD card .IMG file. Any tutorial on flashing an SD card image to physical media will work, but I will tell you the way I like to do it...

**Step 1**

Download and install the software balenaEtcher (avaliable at https://www.balena.io/etcher/. I prefer it to Win32DiskImager, which is reccommended by most tutorials, because it's a lot harder to accidentally wipe an external hard drive or partition) and Tuxera's SD Card Formatter (avaliable at https://www.sdcard.org/downloads/formatter/). Download the SD card image and unpack the archive it's in.

**Step 2**

Insert your pi 4's SD card into your PC. Open up SD card formatter and select your SD card. Make sure it's set to "Quick Format" (unless you have anything super private that needs ABSOLUTE DESTRUCTION), and allow the process to start. Once it's finished open up Etcher. Select the SD card image in the first prompt, and your newly-formatted SD card in the second. Finally, click "Flash". Once it's finished, insert your SD card into your pi.

**Step 3**

Power on your raspberry pi. It will boot straight into Raspbian, due to the lack of the boot manager NOOBS (which is intentional). Once it's started, configure your settings. The default popup that walks you through the process will not pop up, this being a preconfigured image, so you will have to do things a little differently.
     - Go to "Appearance and personlization" and go to Display. It will be set to the lowest resolution by default, so set your screen resolution to match your TV/monitor.
     - Open up a command promptand type "sudo passwd". The default password is "raspberry", so type that in first. Next, type in your desire password. For security reasons, it
       won't let you see what you are typing. Finally, it will ask you to type in your password once more. Once you've done that, you're good to go password-wise!
     - Whilst in the command prompt, type "sudo raspi-config". Configure the settings you want to change, and then select "Exit".
 
That's it! Your system is set up!

**Now what?**

The PORTal comes pre-loaded with Retropie (modified version of EmulationStation tailored to the Raspberry Pi), Dolphn Emulator (GC/Wii emulator, though only GC works at this time), Chromium (a web browser), a 64-bit CHROOT (required for Dolphin), Anbox (for android apps), and much more! Matchbox keyboard is included, but you can plug in a physical keyboard if it better suits your fancy. I also left room for additional programs and games, should you need them. Finally, this image containes NO ROMS OF OFFICIAL GAMES!!! Such practice would be considered piracy, and the last thing I need is a cease-and-desist from Nintendo. Homebrew games and apps are different and may be included with future releases.
