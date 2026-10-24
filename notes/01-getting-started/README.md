# 01 · Getting Started

Linux distributions, installing Linux in a VM, and logging in.

## Notes

Read in this order:

1. **[Linux distributions](linux-distributions.md)**: what a distro is, the main families, and which one to learn

## Summary

The key facts from this topic, one line each.

- Linux itself is only the **kernel**. A distribution adds the shell, commands, package manager and settings around it.
- Distributions share the same kernel, mostly the same commands and the same directory layout, so skills carry over between them.
- The biggest real difference between families is the **package manager**.

## Quick reference

The commands covered in this topic, with the note that explains each one.

### [Linux distributions](linux-distributions.md)

- `cat /etc/os-release`: name, version and ID of the distribution. Works on almost every modern distro.
- `hostnamectl`: OS name, kernel and hostname together.
- `uname`: kernel name only, which is `Linux`.
- `uname -r`: kernel version only.
- `cat /etc/redhat-release`: release name on the Red Hat family only.
- `lsb_release -a`: release details on Debian and Ubuntu.
- `. /etc/os-release`: load the file's values as shell variables such as `$ID` and `$ID_LIKE`, for use in scripts.

---

[All topics](../../README.md#topics) · [02 · Filesystem](../02-filesystem/README.md) →
