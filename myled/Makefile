# SPDX-License-Identifier: GPL-3.0
# *Copyright (c) 2021 Ryuichi Ueda and RikoBato. All rights reserved.
obj-m :=myled.o
myled.ko: myled.c
	make -C /usr/src/linux-headers-`uname -r` M=`pwd` V=1 modules
	gcc NumerOn.c -o numeron
clean:
	make -C /usr/src/linux-headers-`uname -r` M=`pwd` V=1 clean
	rm numeron
