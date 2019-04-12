<!-- TITLE: Modding Linux -->
<!-- SUBTITLE: Get Beat Saber Mods working on Linux! -->

# Beat Saber Modding on Linux
For those running Linux willing to mod their BeatSaber installation, there are 2 easy ways to do it. We will assume you know advanced stuff already, so we won't go into much detail on some steps.

There are two ways to do it, depending on the presence of Windows as a dual boot on your system.

Thanks to `R3D#3441` on Discord for making this guide! 

## Dual Boot with Windows installation

1. Mod the game under windows using either one of the provided mod managers, or by doing it manually. Once you are done, copy the contents of the Beat Saber folder onto a USB drive or a partition that linux could read. 

2. Boot Linux, and paste the contents of the USB into the BeatSaber folder of your linux machine.

3. Start Steam, start the game and enjoy your newly modded game on your FOSS platform! 

## No Dual Boot

You will need a Windows VM for this, you can create one pretty easily and for free using VirtualBox and a Windows 10 ISO from Microsoft's website (no need to activate it)

1. Quit Steam, move your Beat Saber folder into a shared folder of the VM, and download one of the mod managers in the Windows VM. 

2. Launch the mod manager in the Windows VM, it will give you an error telling you that it did not find your Beat Saber installation. Just accept and select the Beat Saber folder in the shared folder of the VM.

3. Mod the game as you normally would (VM needs internet access to do so) and then shut down the VM, move the BeatSaber folder back to where it originally was on your system and launch Steam.

4. Your game should now be modded and should launch and load mods.

PS: There used to be a way to do this using Wine, but the newer versions of .NET are troublesome and running a mod manager or BSIPA with Wine WILL NOT WORK!