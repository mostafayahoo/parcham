# bamanbekhan

>┌─[alfa@parrot]─[~/Downloads/parcham/3]\
└──╼ $file bamanbekhan\
bamanbekhan: data
#
>┌─[alfa@parrot]─[~/Downloads/parcham/3]\
└──╼ $dd if=bamanbekhan of=./extract.squashfs skip=40 bs=1\
15524518 bytes (16 MB, 15 MiB) copied, 129 s, 120 kB/s
15634432+0 records in
15634432+0 records out
15634432 bytes (16 MB, 15 MiB) copied, 129.916 s, 120 kB/s

#

>┌─[alfa@parrot]─[~/Downloads/parcham/3]\
└──╼ $unsquashfs ./extract.squashfs\ 
Parallel unsquashfs: Using 4 processors
1 inodes (128 blocks) to write
[===============================================================|] 128/128 100%
created 1 files
created 1 directories
created 0 symlinks
created 0 devices
created 0 fifos
#

>┌─[alfa@parrot]─[~/Downloads/parcham/3]\
└──╼ $cd squashfs-root\
┌─[alfa@parrot]─[~/Downloads/parcham/3/squashfs-root]\
└──╼ $ls\
zero.img

#
>┌─[alfa@parrot]─[~/Downloads/parcham/3/squashfs-root]\
└──╼ $file zero.img \
zero.img: data
#
>┌─[alfa@parrot]─[~/Downloads/parcham/3/squashfs-root]\
└──╼ $binwalk zero.img \
DECIMAL       HEXADECIMAL     DESCRIPTION \
*------------------------------------------------------------------------------*\
90969         0x16359         Copyright string: "copyright/trademark/acute/dieresis/.notdef/AE/Oslash"
126311        0x1ED67         Copyright string: "copyright/trademark/acute/dieresis/.notdef/AE/Oslash"
156981        0x26535         Copyright string: "copyright 16#00a9"
157000        0x26548         Copyright string: "copyrightsans 16#f8e9"
157023        0x2655F         Copyright string: "copyrightserif 16#f6d9"
#

>┌─[alfa@parrot]─[~/Downloads/parcham/3/squashfs-root]\
└──╼ $sudo mount zero.img "/mnt\
[sudo] password for alfa: \
┌─[alfa@parrot]─[~/Downloads/parcham/3/squashfs-root]\
└──╼ $
#
>┌─[alfa@parrot]─[~/Downloads/parcham/3/squashfs-root]\
└──╼ $cd /mnt\
┌─[alfa@parrot]─[/mnt]\
└──╼ $ls\
 rand_  'rand_'$'\001''.img'  'rand_'$'\002''.img'  'rand_'$'\003''.img'\
┌─[alfa@parrot]─[/mnt]\
└──╼ $
#

# *open file rand_ and capture the flag*

this file is a postscript 

>>*parcham{I_l0v3_for3n5ics_to0}*
