# JMR 815
Jio Mobile Hotspot Device : JMR 815

Device offered by Jio , runs on 4G LTE network. Provides access to VoLTE using its official app.

# Board: ALT3800 Ver: 0.16 (CPU Speed 396.500 MHz)
# DRAM:  128 MiB (LPDDR, 16-bit, 199.333 MHz, FM61D2G1GA)


# Bootloader:
U-Boot 2012.10-svn3034 (Sep 29 2017 - 15:40:21)

# Wireless driver:
rtl8192es

# OS:
Modified OpenWRT ( Apparently)

# MTD Partitions:
dev:    size   erasesize  name
mtd0: 00080000 00020000 "spl"

mtd1: 000c0000 00020000 "uboot1"

mtd2: 000c0000 00020000 "uboot2"

mtd3: 00040000 00020000 "env"

mtd4: 00040000 00020000 "backup_env"

mtd5: 00300000 00020000 "nvm"

mtd6: 00400000 00020000 "kernel1"

mtd7: 00040000 00020000 "dtb1"

mtd8: 02800000 00020000 "rootfs1"

mtd9: 00400000 00020000 "kernel2"

mtd10: 00040000 00020000 "dtb2"

mtd11: 02800000 00020000 "rootfs2"

mtd12: 00400000 00020000 "modem_fw1"

mtd13: 00400000 00020000 "modem_fw2"

mtd14: 00a00000 00020000 "ua"

mtd15: 09000000 00020000 "tstorage"

# Debugging:
Either using telnet or dropbear. Device provides a USB Ethernet if connected via USB. init.d scripts are available to start telnetd as a service.

# Beware:
Device resets configuration files if the word length does not match with the default backup of the said configuration.

Min Configuration required to initiate the Wireless at wlan0 without which wireless interface is not initiated (needs more debugging)

# Fun things:
Device can be forced into 40Mhz bandwidth effectively doubling the WiFi link speed. Without any special modification.

# TODO :
1. Manage to get WiFi STA working. 
2. USB Ethernet as DHCP client
3. Extract LTE firmware and/or document communication using AT Codes
4. Build a pure OpenWRT image for the device with the latest code.
5. Modify U-Boot with the latest code. 
6. Use the keys and credentials inside the device to download firmware image from Jio


