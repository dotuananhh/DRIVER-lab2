

MODULE_NAME := bai2

obj-m := ${MODULE_NAME}.o

KDIR := /lib/modules/`uname -r`/build

string ?= do tuan anh
endc ?= 0
s1 ?= do
s2 ?= anh

all:
	make -C ${KDIR} M=`pwd`

clean:
	make -C ${KDIR} M=`pwd` clean

install:
	sudo dmesg -C
	sudo insmod ${MODULE_NAME}.ko string='"${string}"' endc=${endc} s1='"${s1}"' s2='"${s2}"'
	sudo rmmod ${MODULE_NAME}
