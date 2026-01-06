# CRLF LF Shenanigans (Flutter Edition)

Oh, hey! There is a new flutter version available, to update simply run `flutter upgrade` ^^
Have you ever tried updating flutter from within WSL in VSCode? Well, I did and it messed everything up...

If you see something like
```bash
/usr/bin/env: ‘bash\r’: No such file or directory
/usr/bin/env: use -[v]S to pass options in shebang lines
```

then it means that (in my case flutter) has now Windows line endings and flutter daemon fails to launch. But worry you not, here is a simple fix for ya!

```bash
sudo apt install -y dos2unix
dos2unix ~/.flutter/flutter/bin/flutter
dos2unix ~/.flutter/flutter/bin/internal/*
```

or recursively

```bash
find ~/.flutter/flutter/bin -type f -exec dos2unix {} \;
```

then ideally restart WSL/VSCode
```bash
wsl --shutdown
```

and check how flutter's doing
```bash
flutter doctor
```

