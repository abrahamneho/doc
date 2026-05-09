sudo apt update
sudo apt install -y build-essential bison flex libelf-dev libssl-dev \
libncurses-dev bc grub2 grub-pc xorriso wget tar gawk texinfo libcrypt-dev mtools

mkdir ~/myos
cd ~/myos
wget https://cdn.kernel.org/pub/linux/kernel/v6.x/linux-6.18.27.tar.xz
tar -xf linux-6.18.27.tar.xz
cd linux-6.18.27
make defconfig
make -j$(nproc)

cd ~/myos
wget https://ftp.gnu.org/gnu/glibc/glibc-2.39.tar.xz
tar -xf glibc-2.39.tar.xz
mkdir glibc-build
cd glibc-build
../glibc-2.39/configure --prefix=/usr --disable-werror
make -j$(nproc)
make install DESTDIR=~/myos/rootfs

cd ~/myos
wget https://ftp.gnu.org/gnu/bash/bash-5.3.tar.gz
tar -xf bash-5.3.tar.gz
cd bash-5.3
./configure --prefix=/usr
make -j$(nproc)
make install DESTDIR=~/myos/rootfs

cd ~/myos
wget https://ftp.gnu.org/gnu/coreutils/coreutils-9.4.tar.xz
tar -xf coreutils-9.4.tar.xz
cd coreutils-9.4
./configure --prefix=/usr
make -j$(nproc)
make install DESTDIR=~/myos/rootfs

cd ~/myos
wget https://github.com/slicer69/sysvinit/releases/download/3.08/sysvinit-3.08.tar.xz
tar -xf sysvinit-3.08.tar.xz
cd sysvinit-3.08
make -j$(nproc)
make install DESTDIR=~/myos/rootfs

mkdir -p ~/myos/rootfs/etc
cat > ~/myos/rootfs/etc/inittab << 'EOF'
::sysinit:/bin/mount -a
::respawn:/bin/bash
EOF

cat > ~/myos/rootfs/etc/fstab << 'EOF'
proc    /proc    proc    defaults    0 0
sysfs   /sys     sysfs   defaults    0 0
tmpfs   /tmp     tmpfs   defaults    0 0
EOF

cd ~/myos/rootfs
mkdir -p bin sbin usr/bin usr/sbin lib lib64 etc dev proc sys tmp home root

cd ~/myos
mkdir -p iso/boot/grub

cp linux-6.18.27/arch/x86/boot/bzImage iso/boot/vmlinuz

cd rootfs
find . | cpio -o -H newc | gzip > ../iso/boot/initrd.img
cd ..

cat > iso/boot/grub/grub.cfg << 'EOF'
set timeout=5
set default=0
menuentry "MyOS" {
    linux /boot/vmlinuz root=/dev/ram0 rw
    initrd /boot/initrd.img
}
EOF

grub-mkrescue -o myos.iso iso/

ls -lh ~/myos/myos.iso
