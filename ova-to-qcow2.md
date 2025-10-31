# Convert OVA to QCOW2

1. Extract the disk image from the OVA file:
```
tar -xvf image.ova
```

2. Convert the disk image to QCOW2 format

install qemu-img first:

Debian/Ubuntu
```
apt install qemu-utils
```

Fedora/RHEL
```
dnf install qemu-img
```

Arch
```
pacman -S qemu-img
```

You can check a list of all disk image formats supported by `qemu-img` with this command:

```
qemu-img -h | tail -n1
```

Now to the actual conversion:

### To convert VDI image to QCOW2 format:

```
qemu-img convert -O qcow2 input.vdi output.qcow2
```

### To convert VMDK image to QCOW2 format:

```
qemu-img convert -O qcow2 input.vmdk output.qcow2
```

##### further read
- https://www.xmodulo.com/convert-ova-to-qcow2-linux.html
