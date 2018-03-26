###############################################################################
1. How to Build
	- get Toolchain
	From android git serveru, codesourcery and etc ..
	- gcc-jopp-only/toolchains/linux-x86_64/aarch64-linux-android-4.9/prebuilt/bin/aarch64-linux-android-

	- edit Makefile
	edit "CROSS_COMPILE" to right toolchain path(You downloaded).
	EX)  CROSS_COMPILE= $(android platform directory you download)/android/prebuilts/gcc-jopp-only/toolchains/linux-x86_64/aarch64-linux-android-4.9/prebuilt/bin/aarch64-linux-android-
	Ex)  CROSS_COMPILE=/usr/local/toolchain/gcc-jopp-only/toolchains/linux-x86_64/aarch64-linux-android-4.9/prebuilt/bin/aarch64-linux-android-		// check the location of toolchain

	- to Build
	$ export ANDROID_MAJOR_VERSION=o
	$ make ARCH=arm64 exynos8895-dream2lte_defconfig
	$ make ARCH=arm64
	
2. Output files
	- Kernel : arch/arm/boot/zImage
	- module : drivers/*/*.ko

3. How to Clean
	$ make clean
################################################################################