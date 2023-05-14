# Steam Deck CFS TKG Tweaks

## Description

The default CPU scheduler in the mainline Linux kernel
is [Completely_Fair_Scheduler (CFS)](https://en.wikipedia.org/wiki/Completely_Fair_Scheduler).

The upstream default settings are tweaked for high throughput which make the desktop applications
unresponsive under heavy CPU loads. This project contains a script that sets the CFS to use same
settings as the [linux-tkg](https://github.com/Frogging-Family/linux-tkg) kernel does.

## Installing

Place `set-cfs-tkg-tweaks.sh` at this directory:
```
/home/deck/.local/bin/set-cfs-tkg-tweaks.sh
```

Place `set-cfs-tweaks.service` at this directory:
```
/etc/systemd/system/set-cfs-tweaks.service
```


## Enabling systemd unit

Tweaks can be applied on boot using provided systemd unit.

```
sudo systemctl enable --now set-cfs-tweaks.service
```

## License

This project is licensed under the [GPL-2.0-only](https://spdx.org/licenses/GPL-2.0-only.html) License - see the COPYING file for details
