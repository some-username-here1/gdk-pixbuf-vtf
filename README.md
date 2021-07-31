## gdk-pixbuf-vtf - Valve Texture Format PixBuf loader

Forrest Voight <voights@gmail.com>
Based on gdk-pixbuf-psd by Jan Dudek <jd@jandudek.com>.

## Installation instructions

```
git clone https://github.com/forrestv/gdk-pixbuf-vtf.git
cd gdk-pixbuf-vtf/
make
sudo cp libpixbufloader-vtf.so /usr/lib/gtk-2.0/2.10.0/loaders/
```

Make sure the above path is correct on your system. Now you need to setup loader with gdk-pixbuf-query-loaders.

### Ubuntu

```
gdk-pixbuf-query-loaders /usr/lib/gtk-2.0/2.10.0/loaders/libpixbufloader-vtf.so \
| sudo tee /usr/lib/gtk-2.0/2.10.0/loader-files.d/gdk-pixbuf-vtf.loaders
```

### Gentoo

```
$ su
# gdk-pixbuf-query-loaders /usr/lib/gtk-2.0/2.10.0/loaders/libpixbufloader-vtf.so \
>> /etc/gtk-2.0/gdk-pixbuf.loaders
```

To enable detection of VTF files in Nautilus:

```
cp x-vtf.xml ~/.local/share/mime/packages/
update-mime-database ~/.local/share/mime/
```
