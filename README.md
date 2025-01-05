# littleOS

A small operating system I wrote following this guide:
https://littleosbook.github.io/

### Setup
#### WSL

#### QEMU


### Running
##### Generate Image:
genisoimage -R                              \
            -b boot/grub/stage2_eltorito    \
            -no-emul-boot                   \
            -boot-load-size 4               \
            -A os                           \
            -input-charset utf8             \
            -quiet                          \
            -boot-info-table                \
            -o os.iso                       \
            iso

##### Run os.iso 
qemu-system-x86_64 -d cpu -D logQ.txt -boot d -cdrom os.iso -m 4 -monitor stdio

### WSL

