# mount-raw

## List or mount partitions within raw disk dumps.

That's pretty much it. 

## Requirements

 * Perl
 * GNU `fdisk` (util-linux)
 * GNU `mount` (util-linux)

## System Requirements for Mounting

 * Kernel loopback (`loop` module) support (enabled by default on most linux distributions)
 * Kernel drivers / userland tools for the filesystem to be mounted, i.e
 * The same drivers you need to access the partitions on real media

## Help

(This README document may be out of date - best check the script itself)

```
mount-raw v0.9 by gammy, github.com/gammy/mount-raw
List or mount partitions within raw disk dumps.

Usage: mount-raw <file> [<partition> <mountpoint>]

If only <file> is supplied, mount-raw will list available partitions and exit.
If [partition] and [mountpoint] are also supplied, the partition is mounted.

Examples:
  mount-raw foo.img              # List partitions in foo.img
  mount-raw foo.img 2 /mnt/tmp/  # Mount partition 2 in /mnt/tmp/

mount-raw will try to use 'sudo' / 'doas' when mounting under a non-root user.
Mounting will ALMOST DEFINITELY only work on Linux as it depends on loopback
support both in the mount (util-linux) command, and the 'loop' kernel module.

Use of this source code is governed by the Simplified BSD License:
https://opensource.org/license/bsd-2-clause
```

## Contact

You can reach me via github: [https://github.com/gammy](https://github.com/gammy)
