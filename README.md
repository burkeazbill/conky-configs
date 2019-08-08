# Burke's Conky configs

My Conky Config Files!
For Windows hosts/servers, I have used DesktopInfo and BGInfo for many years now. For Linux, Conky is a great equivalent. There are a considerable number of advanced things you can do with Conky so everyone has their own idea of what they want shown. You can see other examples on the Conky [User Configs page.](https://github.com/brndnmtthws/conky/wiki/Configs)

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

## Additional Resources:

- [Conky Manager 2 (Updated to support new lua config files)](https://github.com/zcot/conky-manager2)
- [Conky](https://github.com/brndnmtthws/conky)
