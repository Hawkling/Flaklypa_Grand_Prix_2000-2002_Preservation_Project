# Installing Flåklypa Grand Prix on Linux

This is a guide for getting Flåklypa Grand Prix running on Linux, using the program [bottles](https://usebottles.com/) to run the game in a lightweigth and (somewhat ) isolated windows environment.

## Installing bottles

You can install bottles using your distros prefferred package manager like `apt` or `dnf`.

However, I recommend installing the [flatpak version](https://flathub.org/en/apps/com.usebottles.bottles):

```bash
flatpak install flathub com.usebottles.bottles
```

This way the game executables are somewhat sandboxed by default, which is always a good idea if you are going to run applications downloaded from the internet.

## Bottle setup

Start the Bottles application.

We will be setting up a new bottle specifically for running the game.

### Creating the bottle

- Create a new bottle by clicking on the `+` icon at the top left.
- Select the `Custom` profile.
- Set `Architecture` to `32-bit`.
- Select the newest `soda` runner available.
- Enable the `Dedicated Sandbox` option to get better isolation between the untrusted `.iso` and `.exe` files we will be downloading and the rest of your system.

> **Note**: Even though these files seem safe and have a relatively low chance of containing malware (an old Norwegian computer game has a very small influence sphere), it is always good to default to safe(r) practices.

### Configuring the bottle

In the menu of the new bottle, scroll down to `Options`, click on `Settings` and make the following changes:

- Set `Windows Version` to `Windows XP`. This hopefully increases compatibility with the game.
- Enable `Discrete Graphics` if you have a graphics card and really want to use it (probably won't matter for this game...). If you have the flatpak version of `bottles` and an Nvidia card, you might have to install the `org.freedesktop.Platform.GL32.nvidia` flatpak extension.
- Set `Synchronization` under `Performance` to `NTSync`, or just `System` if that is your only option.
- Next to `Dedicated Sandbox`, click on the cog icon. Enable `Share Sound`.
- Click on `DLL Overrides` and enter `security`. Hit enter, and make sure it is set to `Native, then Builtin`. This is to let the installer use the bundled `Security.dll`, which is needed in order to complete the installation.
- Click on `Manage Drives`, and delete the `Z` drive. We do this to hinder any applications running in the bottle from accessing our home folder (in case the downloaded game files contain malware).

## Sourcing and preparing the game files

For sourcing the game files we have two main options:

- Spin up the physical discs from the original game.
  - Either dump the disc images `.iso` files, which will allow you to follow the instructions in the rest of this guide.
  - Or try to add mount the disc drive inside the bottle, which in theory should allow you to install and run the game without downloading and using the No-CD-patched executable.
- Alternatively, since you already own a physical copy of the game, you can download disc images of the game that someone else has uploaded, and install a No-CD patch. This will allow you to run the game without inserting a physical CD every time you want to play.
  - This is the approach we will use in this guide.

### Downloading the files

The game files for the gold edition, which this guide covers, can be found at the Internet Archive: <https://archive.org/details/flaklypagullutgave>

Click on `Show all` to bring up the list of file downloads. You'll want to download:

- `FGPGULL1.mdf`
- `FGPGULL1.mds`
- `FGPGULL2.mdf`
- `FGPGULL2.mds`
- `Oppdatering/FGPGOLD_UPD12.exe`
- `Crack/FGP.exe`

### Converting the disc files to ISOs

The `.mdf` format is a proprietary disc image format used to store copies of CDs, DVDs or Blu-ray. The `.mds` files contain metadata obtained from the physical disc.

The Linux kernel doesn't have native support for mounting `.mdf` files directly. The easist method to get something you can mount as a disc image in your filesystem is to convert the `.mdf` and `.mds` files into an `.iso` file.

You can use a CLI tool like `mdf2iso`. Make sure the `FGPGULL1.mdf` and `FGPGULL1.mds` files are in the same folder. Open that folder in your terminal and run:

```bash
mdf2iso FGPGULL1.mdf FGPGULL1.iso
```

Repeat for `FGPGULL2.mdf`.

These `.iso` files are the files you will be mounting when installing the game later.

#### Mounting `.mdf` files directly

Even though Linux doesn't natively support `.mdf` files, you can often mount a `.mdf` file by simply treating it as a ISO9660 file:

```bash
sudo mount -o loop -t iso9660 /path/to/FGPGULL1.mdf /mnt/mdf
```

This often works for simple disc images, but might not be able to decode more complex disc images, such as games containing both game files and sound files. That is when you would need the metadata on the `.mds` file. I have not tried this approach for this game.

## Installing Flåklypa Grand Prix

### Add the game files to the bottle's C drive

Open the bottle's C drive in the file manager by clicking on `Browse` next to `Browse C:/ drive`.

Copy the following files into the C drive, i.e. the `drive_c` folder which you just opened:

- `FGPGULL1.iso`
- `FGPGULL2.iso`
- `FGPGOLD_UPD12.exe`
- `FGP.exe`: No-CD patched executable.

### Mount the iso files inside the bottle

Open a console in the C drive of the bottle. You can usually do that by right clicking in the file manager and select an option like `Open in Console`.

Create a mountpoint for and mount the `FGPGULL1.iso`:

```bash
mkdir mnt1 && sudo mount -o loop FGPGULL1.iso mnt1
```

Create a mountpoint for and mount the `FGPGULL2.iso`:

```bash
mkdir mnt2 && sudo mount -o loop FGPGULL2.iso mnt2
```

### Run the installer

Go back to Bottles, and click `Run Executable...`.

Enter the `drive_c` folder and then the `mnt1` folder. Select `Setup.exe` and click `Run`.

Click through the installer by hitting `Neste`.

When prompted to "Sett in **SVART** Flåklypa...", hit `Bla gjennom` and select the `mnt2` folder. Hit `OK`, and the installation should resume.

> **Note**: You might not need to select the `mnt2/` folder when installing, if you set up the mount points and mount both ISOs before starting the installation, as described above. It seems like the installer will automatically find the second mounted ISO and continue the installation automatically.

Finally, when prompted to "Sett in **HVIT** Flåklypa...", make sure the `mnt1` folder is selected. Hit `OK`, and the installation should complete.

There's no point in trying to start the game yet, so uncheck the `Start Spillet om ...` checkbox and hit `Fullfør`.

#### Cleanup: Unmount the disc images

It is now safe to unmount the disc images.

Open the `drive_c` folder in the terminal.

Run:

```bash
sudo umount mnt1 && sudo umount mnt2
```

### Install the update

Go back to the bottle, click on `Run Executable...`, select the `FGPGOLD_UPD12.exe` in the `drive_c` folder and hit `Run`. The update should finish quickly.

There is still no point in trying to start the game yet, so uncheck the `Start Spillet om ...` checkbox and hit `Fullfør`.

### Getting around CD-COPS

You are now done with the installation of the game. However, the game uses a copyright protection mechanism known as _CD-COPS_, which among other things checks for the presence of a physical CD. If you try to run the game now, you will simply get a popup telling you to insert the game disc.

**The simplest way around this is to replace the `FGP.exe` file with a No-CD version.**

- Navigate to the game folder `drive_c/Program Files (x86)/Flåklypa Grand Prix/` in you file manager.
- Paste the No-CD version of the `FGP.exe` executable that you downloaded from Internet Archive.
- Make sure to `Replace` the original when prompted. 

#### Emulating the physical disc using CDEmu

Another option, which I have not tried out myself, is to mount the `FGPGULL1.mdf` and `FGPGULL1.mds` files using something like [CDEmu](https://cdemu.sourceforge.io/). This will emulate mounting the real physical disc using the metadata stored in the `.mds` files. This way, you should be able to run the game without installing the cracked `FGP.exe` file. Do note, however, that this will require you to mount the disc image with CDEmu each time you want to play the game.

### Run the game

Now, you should be all set for running the game!

Simply go to your bottle, hit `Run Executable...`, navigate to `drive_c/Program Files (x86)/Flåklypa Grand Prix/FGP.exe` and hit `Run`.

> **Tip**: You can add the executable as a shortcut in the bottle. Under `Programs` in the bottle menu, hit `Add Shortcuts...` and select `FGP.exe`.

## Configuration (optional)

Below follows some optional configuration that you can do to improve your experience.

### Adding fullscreen support

If you don't get fullscreen working out of the box (i believe you should if you are using the soda runner), you can try to install a replacement library for the `ddraw.dll` called [cnc-ddraw](https://github.com/FunkyFr3sh/cnc-ddraw).

This implementation has support for various upscaling techniques/shaders, aspect ratios and other tweaks.

It can be installed easily by clicking on the `Dependencies` button under `Options` in the bottle menu. Just search for `cnc-ddraw` and click on the download and install button.

For actually playing around with and selecting the configuration options you can add a shortcut to the cnc-ddraw config tool. The path to it is `/drive_c/windows/system_32/cnc-ddraw config.exe`. Alternatively, you can edit the `ddraw.ini` config by hand.

### Getting winedebug output to a log file

If for some reason you want to debug what is going when you are running the game, there is a convoluted way to get the `winedebug` log written to a file.

- Add a new shortcut targeted at `FGP.exe`.
- Click the three dots next to it.
- Select `Change Launch Options...`.
- Under `Custom Arguments` in the `Command Arguments` box, paste `>../../debug.txt 2>&1`.

Now, go to the bottle's settings, scroll down to `Environment Variables` and add a new `WINEDEBUG` variable. For example, `WINEDEBUG=+loaddll` to show all libraries loaded in when running the game.

The last step is actually running the game:

- Click the three dots next to the debug shortcut you just added.
- Click the little terminal icon to `Launch with Terminal`.
- Play the game and exit it when you think you have logged what you wanted to look at.
- **IMPORTANT**: Close the `EasyTerm` window that opened when you started the game.
- You should now be able to find a `debug.txt` file in the bottle's `/drive_c` folder, which you can get to by clicking the `Browse...` button at the top of the bottle menu.

This debug info might be valuable if you are struggling to get the game running properly on your machine. There are many winedebug options you can enable, so read up on that.
