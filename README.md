# Install :
`insmod ch34x.ko`

# Compile :
```
apt install bc
dpkg -i linux-headers-4.4.35-v7+_4.4.35-v7+-2_armhf.deb

#if insmod error,dmesg says:
#	[241282.009958] ch34x: version magic '4.4.35-v7 SMP mod_unload modversions ARMv7 ' should be '4.4.35_ecoo_81080868 SMP mod_unload ARMv7 p2v8 '
#edit /usr/src/linux-headers-4.4.35-v7+/include/linux/vermagic.h

make -C /lib/modules/4.4.35-v7+/build  M=/root/CH341SER_LINUX  CONFIG_EMBEDDED=y

```



#### https://www.wch.cn/downloads/file/177.html?time=2023-03-03%2008:32:34&code=45fMmw0VFQgU54BCqg8mrgDhfVNu7y2Wz4wVhlVo

```
// ChangeLog 
// 1.0 - 1.1   modified to solve transmition between ch341 and ch341
// 1.1 - 1.2   Support high Linux kernel
Instructions

Note: 1.Please run followed executable programs as root privilege
      2.Current Driver support versions of linux kernel range from 2.6.25 to 3.13.x
      3.Current Driver support 32bits and 64bits linux systems

Usage:
	(load or unload linux driver of CH34x)
	//compile 
	#make
	//load ch34x chips driver
	#make load
	//unload ch34x chips driver
	#make unload
// 1.2 - 1.3 Fix some bugs			

```