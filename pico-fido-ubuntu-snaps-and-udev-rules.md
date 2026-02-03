## Pico Fido may need udev rules for certain snaps - e.g. on Ubuntu

[The Pico Fido project](https://github.com/polhenarejos/pico-fido) recently received 3 [official USB Vendor and Product IDs](https://www.picokeys.com/2026/01/24/picokeys-devices-receive-official-vid-pids/). 

Before that it used the dummy IDs `feff` as Vendor ID and `fcfd` as the product ID.
On Windows 11 that did not cause any issues - nor on Fedora Linux. But for [snap based](https://snapcraft.io/) browsers like on Ubuntu that might create access issues (as Snaps can have reduced access to the system via [confinement](https://snapcraft.io/docs/snap-confinement)).

In those circumstances udev rules might be needed to grant access to the Pico Fido key with the dummy Vendor and Product IDs.

For Chromium in `/etc/udev/rules.d/70-snap.chromium.rules`
```
SUBSYSTEM=="hidraw", KERNEL=="hidraw*", ATTRS{idVendor}=="feff", ATTRS{idProduct}=="fcfd", TAG+="snap_chromium_chromium"
```

For Firefox  in `/etc/udev/rules.d/70-snap.firefox.rules`
```
SUBSYSTEM=="hidraw", KERNEL=="hidraw*", ATTRS{idVendor}=="feff", ATTRS{idProduct}=="fcfd", TAG+="snap_firefox_geckodriver"
SUBSYSTEM=="hidraw", KERNEL=="hidraw*", ATTRS{idVendor}=="feff", ATTRS{idProduct}=="fcfd", TAG+="snap_firefox_firefox"
```
those lines (in Ubuntu 25.10) are sufficient to get a Pico Fido key with the dummy VID and PID recognised by the browsers (Firefox seems to require a line each - tagged for the geckodriver - `snap_firefox_geckodriver` - and firefox itself - `snap_firefox_firefox` compared to one line with only the `snap_chromium_chromium` tag for Chromium).

Hopefully in future the IDs for Pico Fido (real or dummy) will be more widely recognised (even the dummy IDs work on Fedora Linux currently - [as per the Solo Keys documentation it seems to employ a more universal approach to detecting standards compliant tokens](https://docs.solokeys.io/udev/)).

## Important postscript:
N.B. if you want to use a Pico Fido key to protect anything a sophisticated adversary might want to gain access to without leaving any trace - except suggesting you accessed it - then note that [Token2 who do Pico Fido based devices](https://www.token2.com/pico) talk about [a security vulnerablity at the hardware level for Pico based devices](https://www.token2.com/img/T2-SA-RP2350-Dec2025.pdf). There are [various mitigations discussed in a GitHub issue](https://github.com/polhenarejos/pico-fido/issues/187) as well as in [the original paper](https://www.token2.com/img/T2-SA-RP2350-Dec2025.pdf) - but I think the key takeaway - apart from reading the documentation to figure out what mitigations there are - is: **choose a really long PIN - 8 characters as minimum and ensure it is really random (so not birthdays or other numbers personally associated with you and your folks nor anything based off dates in last few hundred years like 19391945 as those restrict the key space in predictable ways)**. 

A strong random PIN combined with resetting your device and passkeys periodically might offer some protection (e.g. if a sophisticated adversary has or can buy access to parallel brute forcing that reduces a theoretical 10 years for an 8 digit PIN down to a few months it will not do them much good if 2 months later your accounts all use different passkeys - i.e. cryptographic keys stored on your physical device - and you have changed the PIN on your security key - i.e. the physical USB or smartcard device). A long PIN would force an attacker to go old fashioned (catch your PIN entry in person or on camera - or gain access to your online accounts via legal coercion of the account provider) or engage in rubber hose cryptography (i.e. torturing you for your PIN - but that would not suit an adversary interested in stealthy acccess or control).

All that said: if you just want to protect an online shopping account or two in a way that is hard to phish then *a FIDO2 security key - even an old FIDO2 security key or a Pico Fido based key when one has not fully read the documentation - might be better than not using passkeys*. As ever this will likely result in attackers in general changing tactics e.g. trying to see if social engineering and identity theft can get them through the account recovery process of a provider - if they can no longer get phishable 2 factor codes due to passkey adoption.
