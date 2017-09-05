# jbod
Manage ZFS disks array with direct SAS attachment on FreeBSD

This script is designed to create and manage ZFS on JBOD disks arrays.
It runs on:
* FreeBSD 9.3
* Dell PowerEdge R620 with LSI SAS 9207-8e HBA
 * 128 Gb RAM
 * Xeon E5-2650 @ 2.00GHz
* Dell PowerVault MD3060e JBOD (60 disks array)

**Install:**
* put "jbod" and "jbod-summary" in "/usr/local/sbin"
* put and edit "jbod.conf" in "/usr/local/etc"
