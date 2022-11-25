I hate it when my SSH service goes down because the network interface was malfunctioning.

To avoid me doing VNC and all the hassle, I made this simple stupid bash script to keep
restart everything that I wanted.

Copy `system-restart` to `$PATH`, do `chmod +x system-restart`.

And use it: `system-restart sshd 0.0.0.0:22`.

It will execute `ss -tlpn` and `grep '0.0.0.0:22'`, if it's empty, it will restart `sshd` service.

[Unlicensed](./LICENSE)