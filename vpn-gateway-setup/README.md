# Setup instructions

Give the machine a static IP or reserve its IP in DHCP and make sure its DNS is set to an external address like `1.1.1.1`

Install programs `openvpn` and  `openssh-server`

Copy `connect.sh`, `iptables.sh` and `auth.txt` to `/etc/openvpn/` and replace **** with proper info

Copy `rc-local.service` to `/etc/systemd/system/`

Copy `rc.local` to `/etc/` then run `chmod +x /etc/rc.local`

Run `systemctl enable rc-local`

Reboot the machine and it should connect automatically
