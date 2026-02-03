## Pico Fido may need udev rules for certain snaps - e.g. on Ubuntu
offic
[The Pico Fido project](https://github.com/polhenarejos/pico-fido) recently received 3 [offical USB Vendor and Product IDs](https://www.picokeys.com/2026/01/24/picokeys-devices-receive-official-vid-pids/). 

Before that it used the dummy IDs feff as Vendor ID and fcfd as the product ID.
On Windows 11 that did not cause any issues - nor on Fedora Linux. But for [snap based](https://snapcraft.io/) browsers like on Ubuntu that might create access issues (as Snaps can have reduced access to the system via [confinement](https://snapcraft.io/docs/snap-confinement).

In those circumstances udev rules might be needed to grant access to the Pico Fido key with the dummy Vendor and Product IDs. The relevant rules files for Chromium and Firefox are found in `/etc/udev/rules.d/70-snap.chromium.rules` and `/etc/udev/rules.d/70-snap.firefox.rules`.
 Hopefully in future the IDs for Pico Fido (real or dummy) will be more widely recognised (even the dummy IDs work on Fedora Linux currently).
