# fatsort

simple utility for sorting files/directories, very useful for devices strictly sorting according to the file allocation table

### Installation
pacman
```
pacman -S fatsort
```
homebrew
```
brew install fatsort
```
check mount points with lsblk
```
lsblk
```
run fatsort to sort files/directories in desired directory (__make sure to replace sdbX with the correct mount point!__)
```
fatsort -D /Music/ -n -c /dev/sdbX
```

##### further read
- https://unixetc.co.uk/2011/09/24/sorting-a-directory-in-the-fat-file-system/
- https://remysharp.com/til/cli/sorting-fat32-sdcard
- https://superuser.com/questions/376577/how-to-reorder-the-files-of-a-fat32-file-system
- https://www.huge-man-linux.net/man1/fatsort.html
- https://formulae.brew.sh/formula/fatsort
