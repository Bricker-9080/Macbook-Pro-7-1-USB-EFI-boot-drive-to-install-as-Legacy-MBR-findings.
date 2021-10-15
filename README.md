# Macbook-Unsupported-Windows
This repositiory will be mainly for people wanting to run windows on a unsupported mac.

How to install Windows CSM/MBR to avoid black screen after drivers install, using a usb on a MacBook Pro 7,1 or known as mid 2010.


Basically with this method we will be using a windows pe environment to allow us to use winntsetup to use a install.esd or .win file. To install windows as csm while booted into efi mode. For some reason macs only see efi/uefi while booted into usb vs older pcs can do both either csm or uefi with a usb drive. What you need to do is boot into a windows pe environment with winntsetup up on the drive if you need one use Direction lite iso which has many recovery tools such as what I’m talking about.
https://1drv.ms/u/s!ArWhGiYHsruWhe4sodgQM-qf6qTw_g?e=2LO4t8
​

**Instructions**​

**Step One**

Flash/write the direction iso or at some point when I release my iso using Rufus or other tool as uefi/gpt. Recommend using a second drive because you will need to wipe one or the other sorry about that. I will try to find a way on not having to erase the whole drive.

**Step Two**

Once done download or use Microsoft Iso of choice Windows 8,1, 10, 7 which ever you want.

**Step Three**

Next open iso you need to use a pc or Mac with windows by the way for this. It might be possible to do this on Mac OS but don’t quite me on that. Alright so mount the iso using explorer and go to the sources folder, once there look for install.esd or install.wim and copy over to the root of the USB.

**Step Four**

Next you need to wait for it to copy then boot into iso on MacBook Pro or Mac wanting to do a csm/mbr install of windows. Boot using usb FireWire, or thunderbolt, probably will work on network boot as well not sure.

**Step Five**

Next you need to follow instructions from this video until the GPT and bootloader part.

**Step Six**

instructions to follow until 7:07 minutes on video.

Don’t worry this will work on windows 10 and 8,1 and 7

**Step Seven**

Once you get to the partition settings stop 🛑⏹ Once at that point you need to change it to MBR partition table. If you have issues like I did you need to go ahead with GPT option and click okay. Once that happens you definitely need to go to the start menu if using direction iso and search for command prompt or find it on the desktop. Follow this to convert to mbr and follow this [instructions on converting to mbr from GPT partition
https://docs.microsoft.com/en-us/wi...management/change-a-gpt-disk-into-an-mbr-disk

**Step Eight**

Once your done with that go ahead and go back to the video at 7:07 and do mbr let it finish. Next you need to shrink the first partition to 300mb and delete it and resize how you need for your main windows install also leave about 400mb unallocated space for system recover etc which should do it on its own after this next step.

**Step Nine**

Alright so for the bootloader you need to use the 300mb ntfs partition, and for the location of install drive use the partition you resized for your windows install. Use the winntsetup video linked earlier if needed.

**Step Ten**

Make sure at the options below location of install drive which last step we did to choose your windows edition like home, pro, etc you want.

**Step Eleven**

Once done with that you need to clock setup and then change boot code uefi to bios.

**Step Twelve**

Once done you can click shutdown after install and do okay. This should take about 20-30 minutes depending on if your using a ssd or hdd

**Step Thirteen**

Once done you can power on the Mac and hold the alt/option key and select windows this should take about 30 seconds to load windows start up if your using a MacBook Pro 7,1 use nvidia 321 drivers others seems to have issues. Also use bootcamp 4.0.4033 this version should work just fine for Nvidia 320m and 9400m models of macs. After installing bootcamp drivers you should update Nvidia drivers to 321 if using a 320 Nvidia gpu. Hope you enjoyed this guide and windows. Let me know if I forget anything or have questions.

NVIDIA 321 drivers
https://www.nvidia.com/download/driverResults.aspx/71706/en-us

BOOTCAMP DRIVERS 4.0.433
https://drive.google.com/file/d/1hkVkGNo4q-viL-7FZu_ptLuBHHKP4EE1/view

Images of successful boot and windows running completely fine with little to no issues. Despite apple saying this machine is unsupported for windows 10 bootcamp

**Links for help or questions
**

https://linktr.ee/Howeitworks

https://www.howeitworks.com/direction

https://discord.gg/tCHPXVKZ
