# Coherent Install
How to install coherent (a unix v7 clone) on qemu

##Installing Coherent from Floppy images in [mwc.tgz](http://www.tuhs.org/Archive/Other/Coherent/Stephen_Ness/) mirrored by TUHS or from [Ness Software](http://www.nesssoftware.com/home/mwc/source.php) onto Qemu.
---

*  Serial number is under http://www.tuhs.org/Archive/Other/Coherent/

1. Copy d1, d2, d3, and d4 from distrib/coherent/4_2_10/ to your working directory as d1.img, etc.
  * for i in 1 2 3 4 ; do cp ${COHERENT}/distrib/coherent/4_2_10/d${i} ${WORK}/d${1}.img
1. Create virtual drive(s) for your installation.
  * for i in 1 2 3 ; do qemu-img create -f raw coherent${i}.img 128M; done
1. 






### Notes:
 * I tried to use virtualBox first but ran into issues supporting this 32 bit OS under 64 bit OSX Yosemite.
