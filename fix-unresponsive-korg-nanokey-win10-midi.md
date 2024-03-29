## NanoKey stops working with Windows 10 - the issue

My KORG Nanokey used to work on Windows 10 - using Ableton Live Lite. However retrying it after a period of time saw it fail to show up in Ableton Preferences MIDI tab - despite lights on the Nanokey when plugged in (showing that it is not a cable issue or an obvious hardware failure).

## NanoKey stops working with Windows 10 - the search results and the problem
Searching saw people refer to Youtube videos such as [https://youtu.be/s9OfxDr8oYQ](https://youtu.be/s9OfxDr8oYQ) [https://youtu.be/18SLcnbqwal](https://youtu.be/18SLcnbqwal) for fixes. These videos discuss things like registry editing -  when the latest KORG USB MIDI drivers have the necessary tool. The videos at least explain what it going on. The issue is that in the registry there is under `Computer\HKEY_LOCAL_MACHINE\Software\Microsoft\Windows NT\CurrentVersion\Drivers32` MIDI inputs labelled `midi`, `midi1`,`midi2` etc up to `midi9`. So there are 10 MIDI inputs or channels (midi to midi9) and they may all get occupied with wdmaud.drv (the Windows Audio driver) given as the data value in the registry - or indeed anything other than KORGUM64.DRV (which is the driver indicating that a KORG USB MIDI device is associated with e.g. midi9).

## NanoKey stops working with Windows 10 - the fix
The fix does not involve registry editing. 

1. Open the Windows Start menu and in the KORG folder is a Uninstall KORG USB-MIDI Device utility program.
2. Click that Uninstall KORG USB-MIDI Device utility program and click Next in window that appears. 
3. You should now see a KORG MIDI Driver Uninstall Utility window saying "Please select the midi entry associated with the MIDI device that you want to delete" followed by a list of MIDI entries (midi, midi1, midi2 etc) and the associated devices. If the problem with your KORG Nanokey or similar is the problem I had you will see things like the Nanokey on midi11 or higher (i.e. beyond the 10 that Windows recognises). There is an option button on the screen that if clicked allows you to untick "Delete KORG MIDI Device only" - you may need to untick this - as in my case I needed to untick it to use this utility to untick the MIDI entry associated with a webcamera.
4. So tick all the boxes of the MIDI devices whose entries you wish to delete (enough to leave at least midi9 and maybe more free) then - after checking the devices are unplugged - click Next and exit the utility.

This should leave some MIDI entries between midi1 and midi9 unused - and now reconnecting the KORG Nanokey should see it assigned to midi9 or lower numbered entry - and now if you start Ableton and look in MIDI tab in preferences it should be visible.