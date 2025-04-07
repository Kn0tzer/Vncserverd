<h1>Control your phone with Dopamine from a computer (Remote desktop)</h1>

# You should probably use [this](https://github.com/Kn0tzer/Remote-Control-iPhone) instead

There's an *old* tweak called Screendump that I believe started in either iOS 11 or 12, and has been barely dragged along to sometimes work in rootless iOS 15. This, however, is a guide to get the same functionality on iOS 16 using Dopamine, or in theory any jailbreak (No serotonin doesn't work). Just a warning, I did not create or do any development on this. All I've done is created a condensed guide, easy to follow guide combining knowledge from different posts and tools I've found online. This guide assumes you have *extremely* basic jailbreaking knowledge.<br><br>


- Download Filza and Newterm from Sileo (Trollstore Filza also works)
- Download <a href="https://github.com/Kn0tzer/Vncserverd/releases/download/release/vncserverd.zip">this</a> file on your device
- Once downloaded, press share and tap Filza. It should open to /var/mobile/Documents
- Open newterm and run "cd /var/mobile/Documents"
- Then, run "chmod +x vncserverd" If this is successful, the icon for the file in Filza should have a cog icon in it.
- Hold down on the file in Filza and press move
- Move the file to /var/jb/usr/libexec (or /usr/libexec if on a rootful jailbreak)
- Tap the file and you should get a warning. If you do not get a warning you have done something wrong. Try the steps again or create an issue.
- Tap continue on the warning
- Logs should now open. The remote desktop server is running.
- On your computer, download <a href="https://www.realvnc.com/en/connect/download/viewer/">RealVNC</a>
- Once downloaded, choose continue without an account
- Right click in an empty space and press new connection
- On your phone, open settings and go to wifi. Tap the info icon on the internet you're currently connected to.
- Scroll until you find an ip that looks like 192.168.x.x
- Go back to RealVNC on your computer. In the top box labeled VNC Server, enter that ip address.
- At the 3 tabs on the top, click on Options
- Disable view only
- Back on your phone, open Filza where the log should still be open
- On your computer, click OK to close the tab and double click on the box containing your devices ip. You should now be connected.

Tips: In order to connect, your device must have Filza open with the script running, which can be seen by the logs being active.

If you need to respring your device while connected remotely, respring through Trollstore settings to keep your connection active.
