# 02 · Filesystem

How Linux lays out files, and how to move around, list, find and manage them.

## Notes

Read in this order:

1. **[Directory structure](directory-structure.md)**: the single tree from `/`, what each top-level folder is for, and where apps keep their files

## Summary

The key facts from this topic, one line each.

- Everything lives in one tree that starts at `/`. There are no drive letters, and extra disks appear as folders inside the tree.
- In Linux, everything is a file, including devices and live system information. The main file types are general files, directories and device files.
- Each kind of file has its own place: programs in `/usr` or `/opt`, settings in `/etc`, changing data in `/var`, and personal files in `/home/<user>`.

## Quick reference

The commands covered in this topic, with the note that explains each one.

### [Directory structure](directory-structure.md)

- `ls /`: list the top-level directories.
- `ls -l /`: the same, with details. Shows which directories are symlinks.
- `ls -l / | grep -- '->'`: only the top-level directories that are links into `/usr`.
- `tree -L 1 /`: tree view, one level deep. Install `tree` first.
- `man hier`: the built-in manual page describing the layout.
- `ls /etc/ssh/`: list a service's configuration files.
- `sudo ls /var/log/`: list the log files. Some can only be read by root.
- `cat /proc/version`: the running kernel version.
- `head /proc/meminfo`: the first lines of the memory report.
- `grep -c processor /proc/cpuinfo`: the number of CPU cores.
- `df -h`: which disks and filesystems are mounted where.
- `sudo du -sh /var/log`: how much space a directory uses.

---

← [01 · Getting Started](../01-getting-started/README.md) · [All topics](../../README.md#topics) · [03 · The Shell](../03-shell/README.md) →
