# PFS-BatchKit-Manager
Is a batch script that allows you to easily manage your PS2/PSX hard drive.

![image](https://user-images.githubusercontent.com/22562949/152685787-f7b0dd25-8731-4b13-aa49-e0b9e5ed09c9.png)


# How to use

<details>
  <summary> <h7> <b> How to Install FreeHDBoot (Hack your PS2 hard drive) </b> </h7> </summary>
   <p>
     
IMPORTANT! If you have already Formatted and installed FreeHDBoot (From HDD), you don't need to do this.       
     
If you installed Premade FreeHDBoot image with HDD Raw Copy Please format your hard drive by following all the steps below.

1) In PFS BatchKit Manager Go to `Advanced menu` > `HDD Management`
     
2) Choose option 8 `Hack your HDD To PS2 Format` `(This is only intended to be used as an entry point for the PS2.)`
     
3) After the hacking put your HDD in your PS2 and format your hard drive with wLaunchELF.      
In wLaunchELF do this `FileBrowser` > `MISC` > `HDDManager` > `Press R1` > `Format` and confirm.
     
4) Now `Press R1` > `Create` Type `+OPL` And Select `OK`
    
5) Choose the size of your partition          
   it will depend on your use if you plan to use the Virtual Memory Card for each game it is preferable to have a large partition size     
  
   Choose `768`  if your HDD size is smaller than `500gb`       
   Choose `2560` if your HDD size is larger than `500gb`   
     
   If you do not intend to use the Virtual Memory Card for each game you can choose `512`
     
   Now Press Circle and OK to continue             
   Note: sometimes during the creation of the partition, he will be able to name it in `+OPL1` , it will have to be renamed to `+OPL`
 
6) Copy the contents of the !COPY_TO_USB_ROOT folder to the root of your USB drive                
 `Your usb key must be in FAT32 format`

7) Install FreeHDBoot (From HDD).
In wLaunchELF do this `FileBrowser` > `Mass` > `APPS` > `FreeMcBoot` > `FMCBInstaller.elf` Press Circle for Launch > `Press R1` > `Install FHDB` (From HDD)

8) Your hard drive will be properly formatted and hacked after that
  ------
     
   </p>
</details>


<details>
  <summary> <h7> <b> How to install PS2 Games </b> </h7> </summary>
   <p>
     
NOTE: Before installing your games, it is strongly recommended to create the `+OPL` partition

Support Compressed format Zip, 7z, ZSO
You don't need to convert your BIN/CUE to iso, they will be automatically converted when transferring.

Copy your `.ISO`, `.BIN/CUE`, `.ZSO`, `.Zip`, `.7z` in DVD Folder Or You can choose a folder where your games are located during installation.

In PFS BatchKit Manager Choose `Transfer PS2 Games`
     
  ------
   </p>
</details>


<details>
  <summary> <h7> <b> How to install PS1 Games </b> </h7> </summary>
   <p>
   
NOTE: You need to find the right files to be able to launch PS1 games        
for copyright reasons I cannot provide you with these files:

`POPS.ELF` 	    MD5: `355A892A8CE4E4A105469D4EF6F39A42`            
`IOPRP252.IMG` 	MD5: `1DB9C6020A2CD445A7BB176A1A3DD418`

Copy your .BIN/CUE in POPS Folder
1) Transfer POPS-Binaries
2) Go to the `Advanced menu` > `Conversion`
3) Choose Convert .BIN/CUE To .VCD
4) Create `__.POPS` Partition `Choose an appropriate size according to the number of games you want to install`
5) Transfer your PS1 Games
     
  ------
   </p>
</details>


<details>
  <summary> <h7> <b> How to Install HDD-OSD (Browser 2.0) </b> </h7> </summary>
   <p>

NOTE: You need to find the correct files to be able to install the HDD-OSD.                  
for copyright reasons I cannot provide you with these files:        
`hddosd-1.10-u.7z` MD5: `403202A03B910FB6FBD522D6AB5007E7`
     
1) Install FreeHDBoot (From HDD)
2) Create `+OPL` Partition
3) Go to the `Advanced menu` > `FHDB\HDD-OSD/PSBBN/XMB` Install HDD-OSD
4) In `Partitions Management` Inject OPL-Launcher (For PS2 games you want to run from HDD-OSD)
5) If you want 3D save icons to appear instead of HD-Loader icon Choose Option `9. Update Partition Resources Header`
     
  ------
   </p>
</details>

<details>
  <summary> <h7> <b> How to Setup NBD Server (Network) </b> </h7> </summary>
   <p>

`Obviously this method won't work for PS2/HDD network adapters that don't have a working network port (i.e. gamestar`
       
     
1) Go to `Advanced menu` > `HDDManagement` > `NBD Server`

2) Choose `Install/Update NBD Driver` (You will be asked to restart the computer to activate test mode)

3) After restarting Repeat steps 1 and 2 You will not need to restart your computer this time

4) A window should warn you if you want to install the driver Confirm install the driver                              
(If the driver refuses to install, you will have to go into your computer's bios and disable Secureboot UEFI)

5) After installing the driver Turn on your PS2 go to OPL (Compatible NBD [__Download Here__](https://raw.githubusercontent.com/GDX-X/PFS-BatchKit-Manager/main/PFS-BatchKit-Manager/HDD-OSD/OPNPS2LD.ELF)) 
     
6) In OPL Go to `Settings` > `Enable Write Operation` `ON` Select `OK` For save
   
7) Still in OPL Go to `Network Settings` and write down the `IP Address` Now go back to the menu and Go to `Start NBD Server`       
(if it works, the following message should appear `NBD Server Running...`)     
     
8) Now In PFS Batchkit Manager Go to `Advanced menu` > `HDDManagement` > `NBD Server` > `Mount Device`

9) Type in the IP address of your PS2 that you wrote down                                                       

10) Normally if all goes well, your hard drive should be connected to your pc as local hard drive                    
(You can check in `Show list of mounted devices` InstanceName PS2HDD)
     
Now you can use all features of PFS Batchkit Manager!

NOTE: Once you are done with what you need to do, don't forget to unmount the hard drive from the network

  ------
   </p>
</details>

<details>
  <summary> <h7> <b> How to Show PS1 & PS2 Games in PSBBN & PSX XMB Menu </b> </h7> </summary>
   <p>

1) Connect your PS2 Or PSX HDD With NBD Server Or locally
2) Install PS2 Games
3) Go to the `Advanced menu` > `FHDB\HDD-OSD/PSBBN/XMB` > `Partitions Management` 
4) Choose Convert HDL Partition for PSBBN & XMB Menu

NOTE: For PS1 games you need to install them as a partition everything will be done automatically
     
  ------
   </p>
</details>

<details>
  <summary> <h7> <b> Feature </b> </h7> </summary>
   <p>

- Assign titles database for PS1 Games VCD
 - Assign titles database for PS2 Games during Installation
 - Backup OPL Resource Files ART, CFG, CHT, VMC, THM,
 - Backup PS1 Games to VCD in any __.POPS# Partition
 - Backup PS2 Games to iso
 - Backup POPS VMC
 - Change default directory for iso installation
 - Check MD5 PS2 Games with redump database
 - Connect PS2 HDD to network NBD
 - Convert HDL Partiton for HDD-OSD, PSBBN, XMB Menu
 - Convert PS1 Games to VCD
 - Convert PS2 Games to ZSO
 - Create & Delete Partition
 - Create Cheat file with mastercode
 - Create Virtual Memory Card
 - Create shortcuts PS1 Game for OPL APPS TAB
 - Delete PS1 Games in any __.POPS# Partition
 - Download Applictions, Artwork, Configs, Widescreen
 - Dump your CD-ROM, DVD-ROM PS1 & PS2
 - Dump/Modify Partition Header
 - Export game lists
 - Extract MBR from HDD
 - Format HDD to PS2 Format
 - Hack HDD For As an entry point
 - Hide/Unhide partition
 - Inject OPL-Launcher
 - Install APPS for HDD-OSD, PSBBN, XMB Menu
 - Install HDD-OSD Automatically
 - Mount PFS Partition in windows explorer
 - Rename a title Displayed in HDD-OSD, PSBBN, XMB Menu
 - Rename Automatically all game titles on hard drive with database
 - Show Partition PS1 Games
 - Show Partition PS2 Games
 - Show Partition System
 - Support Compressed format .zip, .7z for PS2 Games
 - Transfer OPL Resource Files ART, CFG, CHT, VMC, THM,
 - Transfer POPS-Binaries
 - Transfer PS1 Games For HDD-OSD, PSBBN, XMB Menu
 - Transfer PS1 Games in any __.POPS# Partition
 - Transfer PS2 Games recursively
 - Transfer PS2 Games To Another PS2 HDD Format
 - Update Partition Resources Header for HDD-OSD, PSBBN, XMB Menu

  ------
   </p>
</details>

# FAQ

<details>
  <summary> <h7> <b> PSX DESR compatible? </code>  </b> </h7> </summary>
   <p>

  Yes, all models are supported
  
  PSX V1 5000, 7000, 5100, 7100                
  PSX V2 5500, 7500, 5700, 7700
  
  NOTE:
  In HDD Management menu                     
  Do Not Format your PSX hard drive           
  Do Not Use Option Hack PS2 HDD
  
  For security, I advise you to make a full backup of your PSX hard drive in case of problems. You can do it with HDDRawCopy
  
 ------
   </p>
</details>

<details>
  <summary> <h7> <b> Things not to do </code>  </b> </h7> </summary>
   <p>
     
  Do not use the Expand option in wLaunchELF, it may corrupt your hard drive 
  
  ------
   </p>
</details>

<details>
  <summary> <h7> <b> I'm stuck during file transfer </code>  </b> </h7> </summary>
   <p>
  
If you get stuck during file transfer, it means your partition is full or corrupted.

You have to delete it and recreate one with an appropriate size

 ------
   </p>
</details>


<details>
  <summary> <h7> <b> Can use it without internet ?  </b> </h7> </summary>
   <p>
     
  Yes you can use it without internet
     
  ------
   </p>
</details>

<details>
  <summary> <h7> <b> Can I use my 1TB, 2TB hard drive? </b> </h7> </summary>
   <p>

Yes Support up to 2TB Maximum
     
  ------
   </p>
</details>

<details>
  <summary> <h7> <b> What is <code>TROJAN_7.BIN</code>  </b> </h7> </summary>
   <p>
     
It's a patch for PS1 games that fixes some bugs.
     
you can find it [__here__](https://www.psx-place.com/threads/popstarter.19139/page-8#post-298564)
     
  ------
   </p>
</details>

<details>
  <summary> <h7> <b> Screenshots </b> </h7> </summary>
   <p>

![image](https://user-images.githubusercontent.com/22562949/152686188-325fe89d-c02c-4908-a517-2751774fcc9f.png)
     
![image](https://user-images.githubusercontent.com/22562949/152685686-1a12ed0d-93fc-4eeb-8971-28fb0db95152.png)
     
![PFSInstall](https://user-images.githubusercontent.com/22562949/177049531-475f18ad-f0d6-4d7f-9d9e-4eb93b39ee94.png)

![ae3d5a45181942f225fe4657b1b0a8d8](https://user-images.githubusercontent.com/22562949/170713114-5154c779-92f6-4917-bf83-89f2bd313396.png)

![PSX_XMB_Games_Final_1_Cropped](https://user-images.githubusercontent.com/22562949/170713170-a96cf172-879b-43ae-9863-044e7182452e.png)


  ------
   </p>
</details>

<details>
  <summary> <h7> <b> Special Thanks </b> </h7> </summary>
   <p>
 
AkuHAK, Roland, Uyjulian For maintaining and improving hdl_dump and pfsshell.

NeMesiS, Dekkit Rs1n For making me want to create this script.

krHACKen For mbr.img and POPStarter and CUE2POPS

El_isra For POPS-VCD-ID-Extractor and DiagBox.

LopoTRI For the tests carried out.

TnA For giving me some ideas to add to the script.

Roland For NBD Server

SpaceCoyote For PS1 games covers HDD-OSD

Thanks to the other people I may have forgotten who have contributed to the PS2 scene!

  ------
   </p>
</details>
