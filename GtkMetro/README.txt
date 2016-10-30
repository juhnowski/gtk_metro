​Тестировалось на Debian jessie + Gnome

Компиляция(все под рутом)
http://www.gtk.org/download/linux.php
1) http://ftp.gnome.org/pub/gnome/sources/glib/2.50/
autogen.sh
- libffi-dev
- libmount-dev
- libblkid-dev
- uuid-dev
make install
./configure
make
make install
ldconfig
2) http://ftp.gnome.org/pub/gnome/sources/pango/1.40/
./configure
make
make install
ldconfig
3) http://ftp.gnome.org/pub/gnome/sources/gdk-pixbuf/2.36/
-libtiff5-dev
./configure
make
make install
ldconfig
4)http://ftp.gnome.org/pub/gnome/sources/atk/2.22/
./configure
make
make install
ldconfig
5) https://www.python.org/downloads/release/python-2712/
./configure
make
make install
6) http://ftp.gnome.org/pub/gnome/sources/gobject-introspection/1.50/
- flex
- bison
./configure
make
make install
ldconfig
7) http://ftp.gnome.org/pub/gnome/sources/gtk+/3.22/
-libepoxy-dev
./configure --with-gdktarget=linux-fb
make
8) gtk-3-examples
/usr/share/doc/gtk-3-examples/examples
9)
export DISPLAY=":0.0" - прописать в ресурсы, либо выполнять каждый раз перед запуском программы
10)
Построение
gcc -o metro metro.c -Wall `pkg-config —cflags —libs gtk+-3.0` -export-dynamic
11)
Запуск
./metro
результат запуска искать Ctrl+Alt+F1...F7 - команда переключения дисплеев/консолей