## Terraform create debian 12 VM via libvirt

Notes:
This is my first terraform script...

if you get permission denied errors while running this terraform script you need to update host libvirt settings:

```
sudo vim /etc/apparmor.d/libvirt/TEMPLATE.qemu


/var/lib/libvirt/images/**.qcow2 rwk, /var/lib/libvirt/images/**.raw rwk, /var/lib/libvirt/images/**.img rwk,


sudo systemctl restart libvirtd
```