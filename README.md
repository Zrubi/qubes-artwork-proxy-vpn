# NetworkManager VPN status icons

These are custom VPN connection status icons for NetworkManager running in a ProxyVM - in [Qubes OS](qubes-os.org)

This assumes that you are using Qubes OS, you have a separate ProxyVM for VPN connections and [your VPN are handled by NetworkManager](https://www.qubes-os.org/doc/privacy/vpn/)

In this case if you want some nice green/red padlock icon instead of the NetworkManager defaults, follow these instructions:

- [Download the latest release](https://github.com/Zrubi/qubes-artwork-proxy-vpn/archive/master.zip) of this icon pack
- [Copy it to Your ProxyVM](https://www.qubes-os.org/doc/copying-files/)

In Your ProxyVM:

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
