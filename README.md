# Guides Overview
1. [fatsort](https://github.com/bomuhime/notes/blob/main/fatsort.md)
2. [convert ova to qcow2](https://github.com/bomuhime/notes/blob/main/ova-to-qcow2.md)
3. [lenovo bios update on linux](https://github.com/bomuhime/notes/blob/main/lenovo_bios_linux.md)


# Short Commands

### Devcontainers
Set correct permissions for __Devcontainers__ in VSCode if met with `Permission Denied`
```bash
$ chown -R vscode:vscode /workspace/
```

### tshark
Record network traffic with __tshark__ and save it as `.pcap`
```bash
$ tshark -i INTERFACE -w OUTPUT.pcap -F pcap
```
