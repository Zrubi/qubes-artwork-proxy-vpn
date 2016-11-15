# NetworkManager VPN status icons

These are custom VPN connection status icons for NetworkManager running in a ProxyVM - in [Qubes OS](qubes-os.org)

This assumes that you are using Qubes OS, you have a separate ProxyVM for VPN connections and [your VPN are handled by NetworkManager](https://www.qubes-os.org/doc/privacy/vpn/)

In this case if you want some nice green/red padlock icon instead of the NetworkManager defaults, follow these instructions:

- [Download the latest release](https://github.com/Zrubi/qubes-artwork-proxy-vpn/archive/master.zip) of this icon pack
- [Copy it to Your ProxyVM](https://www.qubes-os.org/doc/copying-files/)

**Install the icon pack in Your ProxyVM:**

- Create a directory:

`mkdir -p /home/user/.icons/Adwaita`

- Unzip the icon pack:

`unzip -d /tmp ~/QubesIncoming/<source vm>/qubes-artwork-proxy-vpn-master.zip`

- copy the relevant files into that newly created directory:

`cp -a /tmp/qubes-artwork-proxy-vpn-master/* /home/user/.icons/Adwaita/`

- Reboot Your customized ProxyVM and enjoy the results :)


Yes, this means we just overrideing the default Adwaita icons. Much more elegant solution would be:
- create a real new icon theme
- set this theme as default for your ProxyVM

**Tweaks needed in dom0:**

Since Qubes 3.2 XFCE is the new default Desktop Environment. Related to this change they introduced a new way of tray icon integration. Read `man qubes-guid` for more info. In short you have to swich back to the old tray icon handling in order to keep the padlock icon colors. You can do this by editing `/etc/qubes/guid.conf` and place this line to your ProxyVM (or the global) section:

`trayicon_mode = "border1";`

This way - after you have been rebooted the affected VM(s) - you get back the colorful red/green padlock icons in system tray - enjoy :)
