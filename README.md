# Guides Overview
1. [fatsort](https://github.com/bomuhime/notes/blob/main/fatsort.md)
2. [convert ova to qcow2](https://github.com/bomuhime/notes/blob/main/ova-to-qcow2.md)
3. [lenovo bios update on linux](https://github.com/bomuhime/notes/blob/main/lenovo_bios_linux.md)
4. [crlf lf shenanigans `flutter upgrade` ^^](https://github.com/bomuhime/notes/blob/main/crlf_lf_shenanigans.md)


# Short Commands

### git
Cleanup the local view of the remote and delete local branches that no longer have a remote
```bash
$ git fetch --prune
$ git branch -vv | awk '/: gone]/{print $1}' | xargs -r git branch -D
```

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
### markdown
Create a page break, for example before a heading, useful when generating PDFs
```bash
<div style="page-break-after: always;"></div>
```

### apt
Avoid marking already installed packages as manually installed
```bash
$ sudo apt install --mark-auto <package-name-1> <package-name-2> ... <package-name-n>
```

