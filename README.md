OpenWRT

Builds for Netgear R7800 (Nighthawk X4S AC2600)
https://openwrt.org/toh/netgear/r7800

Based on the work of hnyman
https://forum.openwrt.org/t/build-for-netgear-r7800/316

Features included:

    LuCI with HTTPS SSL support
        LuCI statistics include CPU frequency scaling graph and CPU temp graph
        Luci theme "material" included in addition to the default "bootstrap"
    USB storage automounting
        Support for various file systems to enable most drives.
        (ext2/3/4, FAT, HFS+, CIFS/SMB, NTFS, EFI/GUID partitions)
    WiFi, WPS and reset buttons work
    console tools: Nano text editor, htop, patch, ccrypt for file encryption/decryption
    failsafe entrance trigger time window increased to 5 sec (from 2 s)
    irqbalance for balancing irq load between CPU cores. Initially disabled in config.
        see "cat /proc/interrupts" for summary of irq usage of CPU cores

Network tools

    SQM-scripts for QoS traffic control. The package is initially disabled, as max speed needs to be adjusted to WAN connection speed
    Adblock package (initially disabled)
    IPv6: tunnel support for 6in4, 6to4, 6rd, IPv6 NAT support
    wireguard VPN support (in master)
    kmod-tun, enables opkg install of OpenVPN (openvpn-openssl variant)
    DDNS support
    miniupnpd settings: leave upnp off by default in /etc/config/upnp
    IEFT BCP38 support
    wget, curl
    iptables-mod-ipsec and kmod-ipt-ipsec
    Wake-on-LAN LuCI module

Noteworthy recent changes:

    April 2019: vsftpd removed
    February 2020: wireguard added
