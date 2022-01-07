# Disk and Partition Management

## Useful Commands
- get disk UUID (for fstab): `blkid`

## fstab

## dd
- https://wiki.archlinux.org/title/Dd

## LVM
- see https://wiki.archlinux.org/title/LVM
- see https://wiki.archlinux.org/title/Dm-crypt/Encrypting_an_entire_system#LVM_on_LUKS

### Creation Commands
- create physical volume: `pvcreate /dev/<partition>`
- create volume group: `vgcreate <volume_group_name> /dev/<partition>` (same `<partition>` as for the physical volume)
- create logical volume with fixed size: `lvcreate -L <size>G <volume_group_name> -n <logical_volume_name>`
- create logical volume with percentage of free size (100 for remaining size): `lvcreate -l <site_in_percent>%FREE <volume_group_name> -n <logical_volume_name>`
- format with ext4: `mkfs.ext4 /dev/<volume_group_name>/<logical_volume_name>`

### List Commands
- list physical volumes: `pvs`
- list volume groups: `vgs`
- list logical volumes: `lvs`
- details about volume groups (including allocated and remaining space): `vgdisplay`
- details about logical volumes: `lvdisplay`

### Snapshots
- https://wiki.archlinux.org/title/LVM#Snapshots

### Resizing
- https://wiki.archlinux.org/title/LVM#Resize_physical_volume
- https://wiki.archlinux.org/title/Resizing_LVM-on-LUKS