```bash
sudo apt install qemu-system virt-manager virt-viewer dnsmasq vde2 bridge-utils netcat-openbsd # install necessary packages
sudo systemctl start libvirtd # self-explanatory
sudo systemctl status libvirtd # also self-explanatory
```

Edit the `/etc/libvirt/libvirtd.conf` file to allow users to use `kvm`

In the file, look out for these and make sure they match.

- `unix_sock_group = "libvirt"`
- `unix_sock_ro_perms = "0777"`
- `unix_sock_rw_perms = "0770"`

![[libvirt_config_user.png]]

Next, include your user into the libvirt group.
```bash
sudo usermod -aG libvirt $USER
```

Restart the `libvirtd` daemon

```bash
sudo systemctl restart libvirtd
sudo systemctl status libvirtd 
```

Start Virt-Manager

> [!note] Note
> 	If you are met with the "no connection error", just double click the `QEMU/KVM - Not Connected` button

