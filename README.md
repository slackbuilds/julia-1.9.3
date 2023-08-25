## Julia

A julia-1.9.3 build script.

```
bash-5.1$ diff julia.SlackBuild.orig julia.SlackBuild
28c28
< VERSION=${VERSION:-1.3.1}
---
> VERSION=${VERSION:-1.9.3}
95a96,101
> mkdir -p $PKG/usr/share/icons/hicolor/48x48/apps
> cp -a $CWD/julia.png $PKG/usr/share/icons/hicolor/48x48/apps/julia.png
> # Specify the full path and file extension.
> sed -i "s#Icon=julia#Icon=/usr/share/icons/hicolor/48x48/apps/julia.png#g" \
> $PKG/usr/share/applications/julia.desktop
>
104c110
< cat $CWD/$PRGNAM.info > $PKG/usr/doc/$PRGNAM-$VERSION/$PRGNAM.info
---
> # cat $CWD/$PRGNAM.info > $PKG/usr/doc/$PRGNAM-$VERSION/$PRGNAM.info
bash-5.1$
```
