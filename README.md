# NetworkManager VPN status icons

These are custom VPN connection status icons for NetworkManager running in a ProxyVM - in Qubes OS.

This assumes that you are using Qubes OS, you have a separate ProxyVM for VPN connections and your VPN are handled by NetworkManager:
https://www.qubes-os.org/doc/privacy/vpn/

In this case if you want some nice green/red padlock icon instead of the NetworkManager defaults, follow these instructions:

- Download the latest release of this icon pack
- Copy it to Your ProxyVM:
  https://www.qubes-os.org/doc/copying-files/

In Your ProxyVM:

- Create a directory: 
  mkdir -p /home/user/.icons/Adwaita

- Unzip the icon pack into that newly created directory.

- Reboot Your customized ProxyVM and enjoy the results :)
