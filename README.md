# jbod
Manage ZFS disks array with direct SAS attachment on FreeBSD

This script is designed to create and manage ZFS on JBOD disks arrays.
It runs on:

* FreeBSD 9.3

* Dell PowerEdge R620:
  * 128 Gb RAM
  * 2 x Xeon E5-2650 @ 2.00GHz
  * PERC H310 Mini (internal)
  * LSI SAS 9207-8e HBA with dual SAS link on JBOD
  * 2x 160 SAS disks for system, RAID 1, on internal RAID controler (PERC H310)

* Dell PowerVault MD3060e JBOD (60 disks array)

* ZFS:
  * 1 ZPOOL => 9 RAIDZ2 vdevs of 6 disks (600 Gb 2.5 SAS @ 10Krpm /) => 54 disks / JBOD
  * 2 x 600 Gb 2.5 SAS @ 10Krpm (spare / JBOD)
  * 2 x 8 Gb ZeusRAM for ZIL / JBOD
  * => 2 free slots on JBOD
  * One 200 Gb SSD for L2ARC on internal RAID controler (PERC H310)

**Install:**
* put "jbod" and "jbod-summary" in "/usr/local/sbin"
* put and edit "jbod.conf" in "/usr/local/etc"
