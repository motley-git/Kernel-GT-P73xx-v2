HOW TO BUILD KERNEL 2.6.36

1. How to Build
	- get Toolchain
			From Codesourcery site( http://www.codesourcery.com )
			Ex) Download : http://www.codesourcery.com/sgpp/lite/arm/portal/package7813/public/arm-none-eabi/arm-2010.09-51-arm-none-eabi-i686-pc-linux-gnu.tar.bz2

			recommand :
							Feature : ARM
							Target OS : "EABI"
							package : "IA32 GNU/Linux TAR"

	- edit Makefile
			edit "CROSS_COMPILE" to right toolchain path(You downloaded).
			Ex)  CROSS_COMPILE=/opt/toolchains/arm-eabi-4.4.3/bin/arm-eabi-                 // You have to check.

	- make
			$ cd kernel
			$ make samsung_p4_usa_tmo_defconfig
			$ make
	
2. Output files
	- Kernel : Kernel/arch/arm/boot/zImage
	- module : Kernel/drivers/*/*.ko
	
3. How to make .tar binary for downloading into target.
	- change current directory to Kernel/arch/arm/boot
	- type following command
	$ tar cvf SGH-T859_Kernel.tar zImage
