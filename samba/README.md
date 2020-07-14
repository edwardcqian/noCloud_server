# Local samba file server

Samba is a LAN network file system server. Samba shared directories can be accessed by any OS.

1. Mount local drives
    - Generic Mounting [Instructions](https://www.cyberciti.biz/faq/mount-drive-from-command-line-ubuntu-linux/)
    - NTFS (window filesystem type) Mounting [Instructions](https://www.cyberciti.biz/faq/debian-ubuntu-linux-auto-mounting-windows-ntfs-file-system/)
    - NOTE: when setting up mount on boot via `/etc/fstab/` please remember to test using `sudo mount -a`. If `fstab` is not setup correctly, the OS will not boot properly next time, and you would have to boot in recovery mound and modify fstab (can be a headache).
2. Install samba and add a password protected home folder share, and a public available share folder [instructions](https://linuxconfig.org/how-to-configure-samba-server-share-on-ubuntu-18-04-bionic-beaver-linux)

