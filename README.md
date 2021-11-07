# CFS ZEN tweaks

## Description

The default CPU scheduler in the mainline Linux kernel
is [Completely_Fair_Scheduler (CFS)](https://en.wikipedia.org/wiki/Completely_Fair_Scheduler).

The upstream default settings are tweaked for high throughput which make the desktop applications
unresponsive under heavy CPU loads. This project contains a script that sets the CFS to use same
settings as the [linux-zen ](https://github.com/zen-kernel/zen-kernel) kernel does.

## Getting Started

### Dependencies

Runtime dependencies:

* bash
* gawk
* systemd (for systemd unit)

Build dependencies:

* cmake

### Installing

Available on [AUR](example.com).

Also see releases page for built RPM and DEB packages.

You can also build from source using cmake build system.

### Enabling systemd unit

Tweaks can be applied on boot using provided systemd unit.

```
systemctl enable --now set-cfs-tweaks.service
```

## Version History

* 1.0.0
    * Initial Release

## License

This project is licensed under the [GPL-2.0-only](https://spdx.org/licenses/GPL-2.0-only.html) License - see the COPYING file for details
