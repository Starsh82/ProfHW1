# ProfHW1
Домашнее задание №1. Обновление ядра Linux Ubintu 24.04.

00:29 # uname -r
6.8.0-56-generic

00:39 # dpkg -i *.deb
Выбор ранее не выбранного пакета linux-headers-6.14.0-061400.
(Чтение базы данных … на данный момент установлено 124870 файлов и каталогов.)
Подготовка к распаковке linux-headers-6.14.0-061400_6.14.0-061400.202503241442_all.deb …
Распаковывается linux-headers-6.14.0-061400 (6.14.0-061400.202503241442) …
Выбор ранее не выбранного пакета linux-headers-6.14.0-061400-generic.
Подготовка к распаковке linux-headers-6.14.0-061400-generic_6.14.0-061400.202503241442_amd64.deb …
Распаковывается linux-headers-6.14.0-061400-generic (6.14.0-061400.202503241442) …
Выбор ранее не выбранного пакета linux-image-unsigned-6.14.0-061400-generic.
Подготовка к распаковке linux-image-unsigned-6.14.0-061400-generic_6.14.0-061400.202503241442_amd64.deb …
Распаковывается linux-image-unsigned-6.14.0-061400-generic (6.14.0-061400.202503241442) …
Выбор ранее не выбранного пакета linux-modules-6.14.0-061400-generic.
Подготовка к распаковке linux-modules-6.14.0-061400-generic_6.14.0-061400.202503241442_amd64.deb …
Распаковывается linux-modules-6.14.0-061400-generic (6.14.0-061400.202503241442) …
Настраивается пакет linux-headers-6.14.0-061400 (6.14.0-061400.202503241442) …
Настраивается пакет linux-headers-6.14.0-061400-generic (6.14.0-061400.202503241442) …
Настраивается пакет linux-modules-6.14.0-061400-generic (6.14.0-061400.202503241442) …
Настраивается пакет linux-image-unsigned-6.14.0-061400-generic (6.14.0-061400.202503241442) …
I: /boot/vmlinuz.old is now a symlink to vmlinuz-6.8.0-59-generic
I: /boot/initrd.img.old is now a symlink to initrd.img-6.8.0-59-generic
I: /boot/vmlinuz is now a symlink to vmlinuz-6.14.0-061400-generic
I: /boot/initrd.img is now a symlink to initrd.img-6.14.0-061400-generic
Обрабатываются триггеры для linux-image-unsigned-6.14.0-061400-generic (6.14.0-061400.202503241442) …
/etc/kernel/postinst.d/initramfs-tools:
update-initramfs: Generating /boot/initrd.img-6.14.0-061400-generic
/etc/kernel/postinst.d/zz-update-grub:
Sourcing file `/etc/default/grub'
Generating grub configuration file ...
Found linux image: /boot/vmlinuz-6.14.0-061400-generic
Found initrd image: /boot/initrd.img-6.14.0-061400-generic
Found linux image: /boot/vmlinuz-6.8.0-59-generic
Found initrd image: /boot/initrd.img-6.8.0-59-generic
Found linux image: /boot/vmlinuz-6.8.0-56-generic
Found initrd image: /boot/initrd.img-6.8.0-56-generic
Warning: os-prober will not be executed to detect other bootable partitions.
Systems on them will not be added to the GRUB boot configuration.
Check GRUB_DISABLE_OS_PROBER documentation entry.
Adding boot menu entry for UEFI Firmware Settings ...
done

00:43 # ll /boot/
total 283508
drwxr-xr-x  4 root root     4096 мая 12 00:43 ./
drwxr-xr-x 23 root root     4096 ноя  3  2024 ../
-rw-r--r--  1 root root   295594 мар 24 18:42 config-6.14.0-061400-generic
-rw-r--r--  1 root root   287562 фев 14 17:04 config-6.8.0-56-generic
-rw-r--r--  1 root root   287537 апр 12 00:44 config-6.8.0-59-generic
drwxr-xr-x  5 root root     4096 мая 12 00:43 grub/
lrwxrwxrwx  1 root root       32 мая 12 00:42 initrd.img -> initrd.img-6.14.0-061400-generic
-rw-r--r--  1 root root 77989178 мая 12 00:43 initrd.img-6.14.0-061400-generic
-rw-r--r--  1 root root 68765244 мая  7 00:20 initrd.img-6.8.0-56-generic
-rw-r--r--  1 root root 68774065 мая  7 00:21 initrd.img-6.8.0-59-generic
lrwxrwxrwx  1 root root       27 мая 12 00:42 initrd.img.old -> initrd.img-6.8.0-59-generic
drwx------  2 root root    16384 ноя  3  2024 lost+found/
-rw-------  1 root root  9979398 мар 24 18:42 System.map-6.14.0-061400-generic
-rw-------  1 root root  9081888 фев 14 17:04 System.map-6.8.0-56-generic
-rw-------  1 root root  9107440 апр 12 00:44 System.map-6.8.0-59-generic
lrwxrwxrwx  1 root root       29 мая 12 00:42 vmlinuz -> vmlinuz-6.14.0-061400-generic
-rw-------  1 root root 15696384 мар 24 18:42 vmlinuz-6.14.0-061400-generic
-rw-------  1 root root 14985608 мар 21 02:34 vmlinuz-6.8.0-56-generic
-rw-------  1 root root 15001992 апр 12 01:25 vmlinuz-6.8.0-59-generic
lrwxrwxrwx  1 root root       24 мая 12 00:42 vmlinuz.old -> vmlinuz-6.8.0-59-generic

00:49 # update-grub
Sourcing file `/etc/default/grub'
Generating grub configuration file ...
Found linux image: /boot/vmlinuz-6.14.0-061400-generic
Found initrd image: /boot/initrd.img-6.14.0-061400-generic
Found linux image: /boot/vmlinuz-6.8.0-59-generic
Found initrd image: /boot/initrd.img-6.8.0-59-generic
Found linux image: /boot/vmlinuz-6.8.0-56-generic
Found initrd image: /boot/initrd.img-6.8.0-56-generic
Warning: os-prober will not be executed to detect other bootable partitions.
Systems on them will not be added to the GRUB boot configuration.
Check GRUB_DISABLE_OS_PROBER documentation entry.
Adding boot menu entry for UEFI Firmware Settings ...
done

00:53 # grub-set-default 0

starsh@UbuntuTestVirt:~$ uname -r
6.14.0-061400-generic
