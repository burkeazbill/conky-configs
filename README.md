# Burke's Conky configs

My Conky Config Files!
For Windows hosts/servers, I have used DesktopInfo and BGInfo for many years now to display system information as an overlay on the desktop. For Linux, Conky is a great equivalent. There are a considerable number of advanced things you can do with Conky so everyone has their own idea of what they want shown. You can see other examples on the Conky [User Configs page.](https://github.com/brndnmtthws/conky/wiki/Configs)

I prefer to keep it simple and show just what is really needed. In my case, my main inspiration comes from the VMware Hands On Labs DesktopInfo config. Here's what I ended up with for my Ubuntu VM (You may need to slightly adjust commands depending on your target OS):

![conky VMware Screenshot](/images/conky-VMware.png)

**FEATURES**
- Aligned bottom-right
- The White Title text is centered and read from ~/podname.txt
- The values of all remaining columns are Right Aligned while their titles are defaulted to the left
- The Storage and Memory lines auto-fill the width of the widget
- Internal IP is the Local Machine IP Address
- Corporate IP is the Corporate Network IP (Requires a call to a corporate page to retrieve that info)
- Public IP is the External, Public Internet IP address of the network connection
- Storage - Shows used/total storage. If use exceeds 90%, text turns red
- Memory - Shows used/total memory. If use exceeds 90%, text turns red
- Status - Displayes contents of ~/status.txt + the file's modified Date and time in MM/DD HH:MM format
-- Status is GREEN if the contents of the status.txt is EXACTLY: Ready
-- Status is RED if the contents of the status.txt is ANYTHING other than: Ready

## Installation

Place the VMware.config file from this repo in your Conky folder (IE: ~/.conky) then use Conky Manager 2 to enable Conky on Boot and select "VMware"
Additionally, place the following two files in your home directory ~/

- podname.txt
- status.txt

**podname.txt** should contain a descriptive title. See the screenshot above. The content of podname.txt for that screenshot was: VMware Livefire

**status.txt** Place the word "Ready" in that (without the quotes) If you want to Status to show GREEN Ready as seen in the screenshot. Otherwise, put ANY OTHER text in there. Use-Case - provide a startup-script that updates the ~/status.txt as it progresses until the final step where it has completed and set the status to "Ready".

## Additional Resources

- [Conky Manager 2 (Updated to support new lua config files)](https://github.com/zcot/conky-manager2)
- [Conky](https://github.com/brndnmtthws/conky)
